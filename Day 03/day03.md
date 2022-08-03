# **Statements and Operators**

**Assignment Operator** : "="

### **Practice Question (Rupees to Dollar Converter)** : 
```
#include <iostream>

using namespace std;

int main() {
    
    // inr to dollar
    
    const double inr_to_dollar {0.013};
    cout<<"Convert Rupees To Dollar"<<endl;
    
    cout<<"Enter The Amount In Rupees : ";
    double INR;
    cin>>INR;
    
    double dollar;
    dollar = INR*inr_to_dollar;
    
    cout<<"Ruppees To Dollar is :$ "<<dollar<<endl;
    
    return 0;    
}
```
