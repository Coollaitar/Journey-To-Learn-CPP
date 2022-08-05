# **Controlling Programming Flow**

### **1) If-Else statement** :
```
#include <iostream>
using namespace std;

int main() {
    
    const int driving_age {16};
    int age;
    
    cout<<"Enter your age: "<<endl;
    cin>>age;
    
    if(age >= driving_age){
        
        cout<<"Yes you can drive"<<endl;
    }else{
        
        cout<<"Comeback in "<<driving_age-age<<" years"<<endl;
    }
    
    return 0;
}
```
### **2) Switch Case Statement** :
```
#include <iostream>
using namespace std;

int main() {
    
    int day_code;
    cout<<"Enter a number:";
    cin>>day_code;
    
    switch(day_code){
        case 0:
        cout<<"Sunday";
        break;
        case 1:
        cout<<"Monday";
        break;
        case 2:
        cout<<"Tuesday";
        break;
        case 3:
        cout<<"Wednesday";
        break;
        case 4:
        cout<<"Thursday";
        break;
        case 5:
        cout<<"Friday";
        break;
        case 6:
        cout<<"Saturday";
        break;
        default:
        cout<<"Illegal Code";
        
    }
    cout<<endl;
}   
```
### **3) Range Based Loop** :
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector <int> vec {1,3,5,15,16,17,18,19,20,21,25,26,27,30,50,55,56,58,100,200,300,400,500,600,700};
    
    int count {0};
    
    for(auto i : vec){
        if(i%3==0 || i%5==0){
            count++;
            cout<<" "<<count;
        }
    }
}
```

### **4) Nested Loops** :
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    
    vector <int> data {}; //intialize vector
    int num_items; //intialize number of items
    
    cout<<"Enter The Number of Items You Want To Enter: ";
    cin>>num_items;
    
    for(int i{1};i<=num_items;i++){ //for loop to enter data_items into vector data
        int data_items {};
        cout<<"Enter Data Items "<<i<<":";
        cin>>data_items;
        data.push_back(data_items); // push back used to enter data into vector
    }

    cout<<"Displaying Histogram : "<<endl;
    
    for(auto val:data){ //vector val
        //to print items of data (vector)
        for(int i {1};i<=val;i++){
            if(i%5==0) //skip this if you want to print just items
                cout<<"@";
            else
                cout<<"*";
        }
        cout<<endl;
    }
    cout<<endl;
    return 0;
}
```

### **5) Program On Nested Loops** :
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    
    int result {};
    
    vector <int> vec {2, 4, 6, 8};
    
    for(size_t i{0};i<vec.size();i++){
        for(size_t j = i+1;j<vec.size();j++){
            result = result + vec.at(i)*vec.at(j);
            
            cout<<result<<endl;
        }
        
    }
    return 0;
}
```
### **6) Section Challenge** :
```
#include<iostream>
#include<vector>

using namespace std;

int main()
{
    char selection{};
    vector<int> numbers{};
    int upgrade{};
    do{
        cout<<"P -print numbers"<<endl;
        cout<<"A -add a number"<<endl;
        cout<<"M -display mean of a number"<<endl;
        cout<<"S -display the smallest number"<<endl;
        cout<<"L -display the largest number"<<endl;
        cout<<"Q -quit"<<endl;
        
        cout<<"enter your choice: ";
        cin>>selection;

        if(selection=='P' || selection=='p'){
            if(numbers.size()==0){
                cout<<"list is empty"<<endl;
            }
            else{
                cout<<"[ ";
                for(auto num: numbers)
                    cout<<num<<" ";
                cout<<"]";
            }
            cout<<endl;
        }

        else if(selection=='A' || selection=='a'){
            cout<<"enter the number: ";
            cin>>upgrade;
            numbers.push_back(upgrade);
        }

        else if(selection=='M' || selection=='m'){
            int mean{};
            if(numbers.size()==0)
                cout<<"cannot calculate mean for zero data"<<endl;
            else{
                int sum{};
                for(auto num: numbers)
                    sum = sum+num;
                cout<<"the mean is "<<static_cast<double>(sum)/numbers.size()<<endl;    
            }
        }

        else if(selection=='S' || selection=='s'){
            if(numbers.size()==0)
                cout<<"cannot detect smallest from an empty list"<<endl;
            int small = numbers.at(0);
            for(auto num: numbers)
                if(num<small)
                    small=num;
            cout<<"smallest number is "<<small<<endl;
        }

        else if(selection=='L' || selection=='l'){
            if(numbers.size()==0)
                cout<<"cannot determine largest for empty list"<<endl;
            int large = numbers.at(0);
            for(auto num: numbers)
                if(num>large)
                    large = num;
            cout<<"the largest number is: "<<large<<endl;

        }

        else{
            cout<<"enter a valid choice please..."<<endl;
        }
        
    }while(selection!='Q' && selection!='q');
    
    
    return 0;
}
```
