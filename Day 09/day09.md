# **OOP - Classes and Objects**

### **1) Account** :
```
#include <iostream>
#include <vector>
#include <string>
using namespace std;

class Account{
public: //*******************//
    //attributes
    string name;
    int accout_number;
    double balance;

    //methods
    bool deposit(double bal) {balance += bal; cout<<"In deposit "<<balance<<endl; }
    bool withdraw(double bal) {balance -= bal; cout<<"In Withdraw "<<balance<<endl; }
        
};


int main() {
    Account frank_account;
    frank_account.name="Frank";
    frank_account.accout_number=12345;
    frank_account.balance=10000.0;
    frank_account.deposit(500);
    frank_account.withdraw(5000);
    
    return 0;
    
}
```
