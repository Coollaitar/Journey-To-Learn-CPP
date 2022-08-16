# **Copy of Constructor** :
```
#include <iostream>
#include <string>

using namespace std;

class Player{

private:
    std::string name;
    int health;
    int xp;

public:

    std::string get_name(){return name;}
    int get_health() {return health;}
    int get_xp() {return xp;}
    Player(std::string name_val = "None",int health_val = 0,int xp_val = 0);
    //copy constructor
    Player(const Player &source);
    //destructor
    ~Player(){cout<<"Destructor called for "<<name<<endl;}
};


Player::Player(std::string name_val,int health_val,int xp_val)
    :name{name_val},health{health_val},xp{xp_val}{
        cout<<"3 arg constructor "+ name<<endl;
}

Player::Player(const Player &source)
    //:name(source.name),health(source.health),xp(source.xp){
        :Player{source.name,source.health,source.xp} {  
        cout<<"Copy of constructor : made a copy of "<<source.name<<endl;
}

int main(){
    
    Player empty{"XXXX",100,50};
    Player my_new_object{empty};
    Player{"Frank"};
    Player{"Frank",100,200};
    
    return 0;
    
}
```

# **Deep Copy Constructor** :
```
#include <iostream>

using namespace std;

class Deep {
  
private:

    int *data;

public:
    void set_data_values(int d) {*data = d;}
    int get_data_values() {return *data;}
    //Constructor 
    Deep(int d);
    //Copy
    Deep(const Deep &source);
    //Delete
    ~Deep();
};

Deep::Deep(int d){
    data = new int;
    *data = d;  
}

Deep::Deep(const Deep &source)
    :Deep{*source.data}{
        cout<<"Copy constructor - Deep Copy"<<endl;
}

Deep::~Deep(){
    delete data;
    cout<<"Destructor freeing data"<<endl;
}

void display_deep(Deep s){
    cout<<s.get_data_values()<<endl;
}

int main() {
    
    Deep obj1 {100};
    Deep obj2 {obj1};
    obj2.set_data_values(1000);
    display_deep(obj1);     
    
}
```    
# **Move Constructor** :
<picture>
#include <iostream>
#include <vector>

using namespace std;

class Move {
  
private:

    int *data;

public:
    void set_data_values(int d) {*data = d;}
    int get_data_values() {return *data;}
    Move(int d);
    Move(const Move &source);//copy ctor
    Move(Move &&source)noexcept;//Move ctor
    ~Move();//destructor
};

//Constructor
Move::Move(int d){ 
    data = new int;
    *data = d;
    
    cout<<"Constructor for: "<<d<<endl;
}

//Copy Constructor
Move::Move(const Move &source)
    :Move{*source.data}{
        cout<<"Copy constructor for: "<<*data<<endl;
}

//Move Constructor
Move::Move(Move &&source)noexcept
    :data{source.data}{
    source.data = nullptr;
    cout<<"Move constructor- moving resource "<<*data<<endl;
    }

//Destructor
Move::~Move(){
    if(data != nullptr){
        cout<<"Destructor freeing data for "<<*data<<endl;
    }else{
        cout<<"Destructor freeing data for nullptr"<<endl;
    }
    delete data;
}


int main(){
    
    vector <Move> vec;
    
    vec.push_back(Move{10});
    vec.push_back(Move{20});
    
}
</picture>
