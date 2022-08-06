# **Character and Strings** :

### **1) C-style Strings** :
```
#include <iostream>
#include <cctype>   // for character based functions
#include <cstring> // for c-style string functions
                  // strlen starts from 1 
using namespace std;

int main() {
    
    char first_name[50] {};
    char last_name[50] {};
    char full_name[50] {};
    char temp[50] {};
    
    cout<<"Enter your first name: ";
    cin>>first_name;
    
    cout<<"Enter your last name: ";
    cin>>last_name;
    
    cout<<"Your first name "<<first_name<<" has size of "<<strlen(first_name)<<" characters"<<endl;
    cout<<"and your last name "<<last_name<<" has size of "<<strlen(last_name)<<" characters"<<endl;
    
    strcpy(full_name,first_name);
    strcat(full_name," "); // concatenate space
    strcat(full_name,last_name); // concatenate last_name
    
    cout<<"Your Full Name is "<<full_name<<endl;
    
    
    cout<<"Enter your full name: ";
    cin.getline(full_name,50);
    cout<<"Full Name: "<<full_name<<endl;
    
    for(size_t i {0};i<strlen(full_name);i++){
        if(isalpha(full_name[i]))
            full_name[i] = toupper(full_name[i]);
      cout<<"Full Name is : "<<full_name[i];   
    }    
}
```
### **2) C++ Strings** :
```
#include <iostream>
#include <string>
#include <cctype>

using namespace std;

int main() {
    
    string s1{};
    s1 ="Aadit";
    
    for(size_t i{0};i<s1.length();i++){
        cout<<s1.at(i);
    }cout<<endl;
    
    //range based loop
    for(auto c:s1){
        cout<<c;
    }
}
```
### **3) Find A Word(Position) from String** :
```
#include <iostream>
#include <string>
#include <cctype>

using namespace std;

int main() {
    
    string s1 {};
    s1 = "This is my world";
    string word{};
    
    cout<<"Enter a word: ";
    cin>>word;
    
    size_t position = s1.find(word);
    
    if(position != string::npos){                                // Check if position is -1 or not
        cout<<"Found "<<word<<" at postion: "<<position<<endl; 
    }
    else
        cout<<"Not Found"<<endl;
}   
```

### **4) Section Challenge** :
```
#include <iostream>
#include <cstring>
#include <vector>
#include <cctype>

using namespace std;

int main() {
    
    string alphabet {"abcdefghijklmnopqurstvwxyzABCDEFGHIJKLMNOPQURSTVWXYZ"};
    string key {"XZNLWEBGJHQDYVTKFUOMPCIASRxznlwebgjhqdyvtkfuompciasr"};
    
    string secret_message {};
    
    cout<<"Enter your secret message: ";
    getline(cin,secret_message);
    cout<<endl;
    
    string encrypted_message {};
    
    cout<<"Encrypting Message....."<<endl;
    
    for(char c: secret_message){                // finding c from string secret_message
        size_t position = alphabet.find(c);     // usigned position will be to store the position of c in the string alphabet
        
        if(position != string::npos){           // if position is not equal to string npos
            char new_char {key.at(position)};   // store the characters of the position in key string into new_char string
            encrypted_message += new_char;      // add new_char to encrypted_message
            
        }else{
            encrypted_message += c;             // else add c to encrypted_message
        }
    }
        
    cout<<"\nEncrypted Message is : "<<encrypted_message<<endl;
    
    cout<<"\nDecrypting Message...."<<endl;
    string decrypted_message {};
    
    for(char c:encrypted_message){
        size_t position = key.find(c);
        
        if(position != string::npos){
            char new_char = alphabet.at(position);
            decrypted_message += new_char;
        }else{
            decrypted_message += c;
        }
    }
    
    cout<<"Decrypted Message : "<<decrypted_message<<endl;
  
    cout<<endl;
    return 0;
    
}
```
