# **Pointers and References** :

### **1) Pointer Declaration** :
```
#include <iostream>
using namespace std;
int main(){
    int *p;
    int score {23};
    p = &score;
    
    cout<<score<<endl;
    cout<<&score<<endl;
    cout<<p<<endl;
    cout<<*p<<endl;
}
  ```
  ### **2) Dereferencing Pointer** :
```  
#include <iostream>
#include <vector>
#include <string>
using namespace std;
int main() {
    vector <string> names {"Aadit","Aditya","Prasad"};
    vector <string> *ptr {&names};
    
    cout<<(*ptr).at(0)<<endl;
    
    for(auto name: *ptr){
        cout<<name;
        cout<<endl;
    }
}
```
### **3) Create storage dynamically** :
```
#include <iostream>
using namespace std;

int main() {
    int size {};
    int *int_ptr {nullptr};
    int_ptr = new int[size];
    cout<<int_ptr<<endl;
    delete[] int_ptr;
}
```
### **4) Array of pointer prints first element of array** :
```
#include <iostream>
using namespace std;
int main() {
    int arr[] {1,2,3};
    cout<<arr<<endl;
    cout<<*arr<<endl;
}
```
### **5) Different types of notation** :
```
#include <iostream>
using namespace std;
int main() {
    int arr[] {1,2,4};
    int *arr_ptr {arr};
    cout<<*arr_ptr<<endl; 
    cout<<arr_ptr[0]<<endl; // Pointer subscript notation
    cout<<*(arr_ptr)<<endl;
    cout<<*(arr_ptr+1)<<endl; // Pointer offset notation
    cout<<*(arr+1)<<endl;     // Array offset notation
    
}
```
### **6) Compare Pointers** :
```
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name1 {"Aadit"};
    string name2 {"Aadit"};
    string *p1 {&name1};
    string *p2 {&name2};
    cout<<boolalpha;
    cout<<(*p1==*p2)<<endl;
    cout<<(p1==p2)<<endl;
    cout<<(name1==name2);    
}
```
### **7) Programme** :
```
#include <iostream>
using namespace std;

void int_data(int *int_ptr){
    *int_ptr *= 2;
}

int main() {
    int value {10};    
    int *int_ptr {nullptr};
    int_data(&value);
    cout<<value<<endl;
    
    cout<<"<------------------>"<<endl;
    
    int_ptr = &value;
    int_data(int_ptr);
    cout<<*int_ptr;
}
```

### **8)
