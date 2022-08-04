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
