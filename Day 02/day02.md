## **Variables and Constants**

### **1) Declare and Intialize variables** :
```
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
 ```
### **2) Datatypes** :
``` 
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
```
### **3) Size of dataTypes and maximum , minimum values of dTypes** :
```  
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
 ```
### **4) Constants** :
 ```
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
 ```
### **Section Challenge** :
``` 
#include <iostream>
using namespace std;

int main() {
    
    int small_rooms {0};
    int large_rooms {0};
    const double small_room_price {25};
    const double large_room_price {35};
    const int validity {30};
    const double taxes {0.06};
    
    cout<<"How many small rooms would you like cleaned? ";
    cin>>small_rooms;
    cout<<"How many large would you like cleaned?";
    cin>>large_rooms;
    cout<<"\nEstimate for carpet cleaning service"<<endl;
    cout<<"Number of small rooms : "<<small_rooms<<endl;
    cout<<"Number of large rooms : "<<large_rooms<<endl;
    cout<<"Price per small room :$ "<<small_room_price<<endl;
    cout<<"Price per large room :$ "<<large_room_price<<endl;
    cout<<"Cost :$ "<<(small_rooms*small_room_price) + (large_rooms * large_room_price)<<endl;
    cout<<"Tax:$ "<<((small_rooms*small_room_price) + (large_rooms * large_room_price))*taxes<<endl;
    cout<<"========================================="<<endl;
    cout<<"Total Estimate :$ "<<(small_rooms*small_room_price) + (large_rooms * large_room_price) + ((small_rooms*small_room_price) + (large_rooms * large_room_price))*taxes<<endl;
    cout<<"This estimate id valid for "<<validity<<" days"<<endl;
    
    return 0;
    
    
}
 ```
### **Section Challenge (Section-7)** :

 ```
#include <iostream>
 
#include <vector>

using namespace std;

int main() {
    
    vector <int> vector1 {};
    vector <int> vector2 {};
    vector1.push_back(10);
    vector1.push_back(20);
    
    //display vector 1
    
    cout<<vector1.at(0)<<endl;
    cout<<vector1.at(1)<<endl;
    cout<<"Size of vector1 : "<<vector1.size()<<endl<<endl;
    
    vector2.push_back(100);
    vector2.push_back(200);
    
    //display vector2
    cout<<vector2.at(0)<<endl;
    cout<<vector2.at(1)<<endl;
    cout<<"Size of vector2 : "<<vector2.size()<<endl;
    
    //declare empty 2D vector
    
    vector<vector<int>> vector_2d;
    
    //add vector1 to vector2d
    //add vector2 to vector2d
    
    vector_2d.push_back(vector1);
    vector_2d.push_back(vector2);
    
    //display elements of 2d vector
    
    cout<<vector_2d.at(0).at(0)<<" "<<vector_2d.at(0).at(1)<<endl;
    cout<<vector_2d.at(1).at(0)<<" "<<vector_2d.at(1).at(0)<<endl<<endl;
    
    //change the vector1
    
    vector1.at(0) = 1000;
    
    //display the vector elements in 2d using at method
    
    cout<<vector_2d.at(0).at(0)<<" "<<vector_2d.at(0).at(1)<<endl;
    cout<<vector_2d.at(1).at(0)<<" "<<vector_2d.at(1).at(1)<<endl;
    
    //display vector1 
    
    cout<<vector1.at(0)<<endl;
    cout<<vector1.at(1)<<endl;
    cout<<"Size of vector 1 is : "<<vector1.size()<<endl;

    return 0;  
}   
```

### **How to take Input in vector** :
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector <int> num {};
    int size {};
    cout<<"Enter size: ";
    cin>>size;
    
    for(int i {0};i<size;i++){
        size_t elements[i];
        cin>>elements[i];
        num.push_back(elements[i]);
          
    }
    for(int i {0};i<num.size();i++){
        cout<<num[i]<<" ";
        
}
    cout<<endl;   
}
```

### **How to print elements of vector** :
```
for(auto c:v){
  cout<<c<<" ";
  cout<<endl;
}
```
