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

