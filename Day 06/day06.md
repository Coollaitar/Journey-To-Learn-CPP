# **Functions** :

### **1) Area of Circle and Volume of Cyclinder** :
```
#include <iostream>

//area of circle and volume of cyclinder

using namespace std;

const double pi {3.14};

double cal_area(double radius){
    return pi*radius*radius;    
}

void area_of_circle() {
    double radius {};
    cout<<"Enter radius of circle: ";
    cin>>radius;
    cout<<"The are of the circle with radius "<<radius<<" is "<<cal_area(radius)<<endl;
}

double cal_vol(double radius,double height){
    return pi*radius*radius*height;
}
    
void volume_of_cyclinder(){
    double radius {};
    double height {};
    cout<<"Enter Radius of Cyclinder: ";
    cin>>radius;
    cout<<"Enter Height of Cyclinder: ";
    cin>>height;
    cout<<"The volume of cyclinder of radius "<<radius<<" and height "<<height<<" is "<<cal_vol(radius,height)<<endl;
}

int main() {
    
    area_of_circle();
    volume_of_cyclinder();
}
```

### **2) Overloading Functions** :
```
#include <iostream>
using namespace std;

void print(int);
void print(double);

void print(int num){
    cout<<"This is an digit: "<<num<<endl;
}

void print(double num){
    cout<<"This is a decimal: "<<num<<endl;
}

int main(){
    print(1);
    print(1.1);
}
```

### **3) Passing Arrays To Functions** :
```
#include <iostream>
using namespace std;
void print_arr(int ,size_t,int);// prototype

void print_arr(int arr[],size_t size,int value){
    
    for(size_t i {0};i<size;i++){
        arr[i] = value;
        cout<<arr[i];
        cout<<endl;
    }
}
int main() {
    
    int my_arr[] {1,2,3,4,5};
    print_arr(my_arr,5,20);
}
```               
