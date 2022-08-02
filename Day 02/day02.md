## **Variables and Constants**

**1) Declare and Intialize variables** :

 #include <iostream>

int main() {
    
    int fav ;
    std::cout<<"Enter Your Favourite Number Between 1 to 100:"<<std::endl;
    
    std::cin>> fav;
    std::cout<<"Amazing thats my fav number too";
    std::cout<<"No really!, "<<fav << "is my fav number"<<std::endl;
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
}  

