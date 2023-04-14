# 4.08 classes, encapsulation, and constructors

- recall that before, we had member variables after a public label. this allowed anyone to access the variable via the . operator

*********private: label*********

- to prevent users from accessing member variables
- anything after a private: label can only be accessed by:
    - constructors
    - member functions
    - destructors
    - friends

***************constructors***************

- to initialize an object with non-default values
- think of them as separate from member functions
    
    **********some key points**********
    
    - has the same name as the class itself
    - never called by a user; it is called by the compiler
    - no return value
- they have to be declared and defined
- we use “ClassName::” in front of the constructor identifier to tell the compiler that we are not defining a function

***************************************const member functions***************************************

- when a normal member function ends with const, this signifies that it cannot alter values for any member variables

***************helper functions***************

- meant to be used by other member functions but not by users
- not const as it changes member variables

************************************************************************************why do we prefix some member function definitions with “::” ?************************************************************************************

- if we want to declare or use functions from a specific class outside of its declaration.