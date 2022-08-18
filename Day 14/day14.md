# **Mystring.h File** :
```
#ifndef _MYSTRING_H
#define _MYSTRING_H

class Mystring{
  
private:
    char *str; //pointer to char that holds a C-style string
public:
    Mystring();             //No-args constructor
    Mystring(const char *s); //Overloaded constructor
    Mystring(const Mystring &source);//copy constructor
    ~Mystring();                    //Destructor
    void display() const;
    int get_length() const;         //getters
    const char *get_str() const;
};

#endif //_MYSTRING_H
```
# **Mystring.cpp File** :
```
#include <iostream>
#include <cstring>
#include "Mystring.h"

//No args constructor
Mystring::Mystring()
    :str{nullptr}{
        str = new char[1];
        *str = '\0';
}

//Overloaded Constructor
Mystring::Mystring(const char *s)
    :str{nullptr}{
        if(s==nullptr){
            str = new char[1];
            *str = '\0';
        }else{
            str = new char[std::strlen(s)+1];
            std::strcpy(str,s);
        }
}

//Copy constructor
Mystring::Mystring(const Mystring &source)
    :str{nullptr}{
        str = new char[std::strlen(source.str)+1];
        std::strcpy(str,source.str);
}
    
//Destructor
Mystring::~Mystring(){
    delete [] str;
}

//Display method
void Mystring::display() const {
    std::cout<<str<<" : "<<get_length()<<std::endl;
}

//length_getter
int Mystring::get_length() const{
    return strlen(str);
}

//string getter
const char *Mystring::get_str() const {return str;}
```
# **main.cpp File** :
```
#include <iostream>
#include "Mystring.h"

using namespace std;

int main() {
    
    Mystring empty;         // no-args constructor
    Mystring larry{"Larry"};//overloaded constructor
    Mystring stooge{larry}; //copy constructor
    
    empty.display();
    larry.display();
    stooge.display();
}
```
