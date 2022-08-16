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
