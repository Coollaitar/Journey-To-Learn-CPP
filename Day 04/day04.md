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
