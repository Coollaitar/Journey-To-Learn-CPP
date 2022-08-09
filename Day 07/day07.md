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
