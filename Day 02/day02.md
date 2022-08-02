## **Variables and Constants**

**1) Declare and Intialize variables** :

 #include <iostream>

int main() {
    
    int room_width;
    int room_length;
    cout<"Enter the width of the room : "<<endl;
    cin>>room_width;
    cout<"Enter the length of the room : "<<endl;
    cin>>room_length;
    cout<<"The area of the room is "<<room_width * room_length<<" sqaure feet."<<endl;
    return 0;

}
 
 **2) dataTypes** :
 
 #include <iostream>

using namespace std;

int main() {
 
    long num1 {1000000};
 
    long num2 {1000};

    long long prod {num1*num2};
 
    unsigned int num3 {0};
 
    signed int num4 {12};
    
    cout<<prod<<endl;
    cout<<num3<<endl;
    cout<<num4;
    return 0;
}  

**3) Size of dataTypes and maximum , minimum values of dTypes ** :
  
#include <iostream>
**#include <climits>**
using namespace std;

int main() {
    cout<<CHAR_MIN<<endl;
    cout<<CHAR_MAX<<endl;
    cout<<INT_MIN<<endl;
    cout<<INT_MAX<<endl;
    cout<<LONG_MIN<<endl;
    cout<<LONG_MAX<<endl;
    return 0;
}
