# 6.01 inheritance

- deriving new classes from existing ones, adding new or extra functionalities to the new ones

******************************base class******************************

- the “parent”
- if you know you will be deriving a child class from a parent, you have to declare all of its member functions as “virtual”
    
    ******************************************virtual keyword******************************************
    
    - essentially lets the compiler know that the method CAN be overwritten in child classes

************************derived/child class************************

```cpp
class Child : public Parent {

}
```

- only functions that will be change need to be redeclared
    - just add an “**override**” keyword at the end of the declaration
        - assuming the virtual is at the front

*********************************************************************child class constructor*********************************************************************

- first you have to call the parent constructor, before initializing variables that specifically belong to the child

```cpp
Child::Child():
Parent{},
child_var{0} {

//the child constructor

}
```

- note that derived classes do not have access to private member variables of the parents

***************************************************protected keyword***************************************************

- just like public and private
- it specifies that protected member variables and functions can be accessed by derived classes but not by users