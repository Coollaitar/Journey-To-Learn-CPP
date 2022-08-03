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

### **1) Expression and Conversion Problem** :
```
#include <iostream>
using namespace std;

int main() {
    
    int num1;
    int num2;
    const int count {2};
    int total;

    cout<<"Enter the Two Numbers : ";
    cin>>num1>>num2;
    total = num1 + num2;
    
    double average {0.0};
    
    average  = static_cast<double> (total)/(count);
    
    cout<<"Average of Two Number is : "<<average<<endl;
    
    return 0;
}
 ```   
