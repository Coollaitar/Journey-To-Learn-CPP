### **1) Returning a Pointer from a Function** :
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

### **2) Section Challenge 12** :
```
#include <iostream>

using namespace std;

void print(const int *const array , size_t size){
    
    for(size_t i {0};i<size;i++)
        cout<<array[i]<<" ";
    cout<<endl;
}

int *apply_all(const int *const array1,size_t size1,const int *const array2,size_t size2){
    int *new_array {};
    new_array = new int[size1*size2];
    int position {0};
    for(size_t i {0};i<size2;i++){   //OUTER FORLOOP WILL LOOP THROUGH EACH ELEMENT OF ARRAY1 AND MULTIPLY IT
        for(size_t j {0};j<size1;j++){
           
            new_array[position] = array1[j]*array2[i];
            ++position;
        }
    }
    return new_array;
}

int main(){
    
    const size_t array1_size {5};
    const size_t array2_size {3};
    
    int array1[] {1,2,3,4,5};
    int array2[] {10,20,30};
    
    cout<<"Array 1: ";
    print(array1,array1_size);
    
    cout<<"Array 2: ";
    print(array2,array2_size);
    
    int *results = apply_all(array1,array1_size,array2,array2_size);
    constexpr size_t result_size {array1_size*array2_size};
    
    cout<<"Result: ";
    print(results,result_size);
    
    cout<<endl;
    
    return 0;
}
```
