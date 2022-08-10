### **Returning a Pointer from a Function** :
```
#include <iostream>
using namespace std;

int *create_array(size_t size,int init_value = 0){
    int *new_storage {nullptr};
    new_storage = new int [size];
    for(size_t i {0};i<size;i++)
        *(new_storage+i) = init_value;
        
    return new_storage;
}

int *display(const int *const array,size_t size){
    for(size_t i {0};i<size;i++)
        cout<<array[i]<<" ";
    cout<<endl;
        
}

int main() {
    int *my_array {nullptr};
    int init_value {};
    size_t size;
    
    cout<<"Enter size of array: ";
    cin>>size;
    cout<<"With what value you want to intialize array?: ";
    cin>>init_value;
    
    my_array = create_array(size,init_value);
 
    cout<<"\n-------------------------"<<endl;
    cout<<endl;
    cout<<"Array is : ";
    display(my_array,size);
    delete [] my_array; 
    return 0;
}
```
