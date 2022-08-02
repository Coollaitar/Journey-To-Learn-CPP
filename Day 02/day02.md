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

**3) Size of dataTypes and maximum , minimum values of dTypes** :
  
#include <iostream>
 
#include <climits>
 
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
 
 **4) Constants** :
 
#include <iostream>

using namespace std;

int main() {
    
    int number_of_rooms {0};
    const double price_per_room {30.2};
    const double taxes {0.06};
    const int validity {30};
    
    cout<<"Enter the number of rooms : "<<endl;
    cin>>number_of_rooms;
    
    cout<<"Number of Rooms are : "<<number_of_rooms<<endl; //number of rooms
    
    cout<<"Price per room :$ "<<price_per_room<<endl; //price per room
    
    cout<<"Cost :$ "<<number_of_rooms * price_per_room<<endl; //cost
    
    cout<<"Taxes :$ "<<number_of_rooms * price_per_room * taxes<<endl; //taxes
    
    cout<<"-------------------------------------------------"<<endl;
    
    cout<<"Total Estimated Value :$ "<<(number_of_rooms * price_per_room) +(number_of_rooms*price_per_room*taxes)<<endl;//final cost
    
    cout<<"This is Estimate is valid for "<<validity<<endl; //validity
    
    return 0;
}
