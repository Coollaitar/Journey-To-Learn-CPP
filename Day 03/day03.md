# **Statements and Operators**

***Assignment Operator*** : "="

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
 
### **2) Use of Bool_alpha** :
``` 
 #include <iostream>
using namespace std;

int main() {
    
    int num1 = 10;
    int num2 = 20;
    
    cout<<boolalpha;
    
    cout<<(num1<num2)<<endl;
}
```

### **3) Logical Operator Wind_Speed and Temperature Question** : 
```
#include <iostream>
using namespace std;

int main() {

    //logical operator code
    bool wear_coat {false}; //set wear_coat as false while intializing
    const double temp_to_wear_coat = 25;
    const int speed_to_wear_coat = 45;
    
    //declare temp and speed of wind
    int temperature {};
    int speed_km_hr {};

    // take input of temperature and speed of the wind
    cout<<"Enter the Temperature and Speed of Weather : ";
    cin>>temperature>>speed_km_hr;
    
    //enter condition in wear_coat
    
    wear_coat = (temperature < temp_to_wear_coat || speed_km_hr > speed_to_wear_coat);
    cout<<"Wear a coat OR ? "<<wear_coat<<endl;
    
    wear_coat = (temperature < temp_to_wear_coat && speed_km_hr > speed_to_wear_coat);
    cout<<"Wear a coat AND ? "<<wear_coat<<endl;
    
    return 0;
}
```

### **Section Challenge (Section 8)** :
```
#include <iostream>
using namespace std;

int main() {
    //conversion values
    
    const int dollar_value {100};
    const int quarter_value {25};
    const int dime_value {10};
    const int nickel_value {5};
    
    int change_amount;
    
    cout<<"Enter a value in cents : ";
    cin>>change_amount;
    
    int balance {},dollar {},quarters {},dimes {},nickels {},pennies {};
    
    dollar = change_amount/dollar_value;
    balance = change_amount - (dollar*dollar_value);
    
    quarters = balance/quarter_value;
    balance -= quarters*quarter_value;
    
    dimes = balance/dime_value;
    balance -= dimes*dime_value;
    
    nickels = balance/nickel_value;
    balance -= nickels*nickel_value;

    pennies = balance;
    
    cout<<"-----------------"<<endl;
    cout<<"dollars:"<<dollar<<endl;
    cout<<"quarter:"<<quarters<<endl;
    cout<<"dimes:"<<dimes<<endl;
    cout<<"nickels:"<<nickels<<endl;
    cout<<"pennies:"<<pennies<<endl;
    
    cout<<endl;
    
    return 0;   
}
 ```   
    
