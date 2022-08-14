# **Constructor** :

### **Delegating Constructor** :
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
    Player();
    Player(std::string name_val);
    Player(std::string name ,int health_val , int xp_val);
};

Player::Player()
    :Player{"None",0,0} {
        cout<<"No args constructor"<<endl;
}

Player::Player(std::string name_val)
    :Player{name_val,0,0}{
        cout<<"One arg constructor"<<endl;
}

Player::Player(std::string name_val,int health_val,int xp_val)
    :name{name_val},health{health_val},xp{xp_val}{
        cout<<"3 arg constructor"<<endl;
}

int main(){
    
    Player empty;
    Player{"Frank"};
    Player{"Frank",100,200};
    
    return 0;
    
}
```
