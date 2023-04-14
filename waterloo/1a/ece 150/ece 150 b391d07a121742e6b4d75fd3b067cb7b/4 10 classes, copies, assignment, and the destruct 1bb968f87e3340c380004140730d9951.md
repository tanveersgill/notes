# 4.10 classes, copies, assignment, and the destructor

*********review*********

- v

*********************************************friend function*********************************************

- if you want some external function to be able to access private variables, you have to declare it as a friend inside the class.
    - for example:
    
    ```cpp
    std::ostream &operator<<(
    std::ostream &out, Pair const &p );
    
    class Pair {
    	public:
    		//constructor would be here
    
    	private:
    		//private stuff
    
    	friend std::ostream &operator<<(
    		std::ostream &out, Pair const &p );
    }
    
    //now, outside of the class, we can define the function:
    
    std::ostream &operator<<(
    std::ostream &out, Pair const &p ) { 
    	out << p.first_ << "," << p.second_;
    	return out;
    }
    
    ```
    
    - note that you still have to declare the function normally, declare as a friend, and then define it
    

*********************************************the destructor*********************************************

- used generally to clean up when a local variable/parameter goes out of scope
- only one, and never takes arguments
- name is the class name prefixed with ~
    - like saying “not the constructor” since the name of the constructor is the class name
- usually we want to use it for dynamically allocated memory

******************************************************************avoiding memory leaks with classes******************************************************************

- memory leaks can happen if you try to initialize an instance of a class with another, but using dynamically allocated memory
    - whenever the compiler tries to call the destructor for each one, the first has the memory deleted. but, since the second has the same dynamically allocated address, when its destructor gets called, there is nothing to delete
        - results in an error
    
    ***************one solution: copy constructor***************
    
    - called when a new instance of a class is declared with an existing instance of the class
        - note that this is for initialization
    
    *********************************************************assignment operator*********************************************************
    
    - while the copy constructor deals with initialization, if you try to use “=” to assign an instance to another, you can overload this operator
        - then, you want to make sure to deallocate the information already in the variable being assigned to before moving information over

************************what if you don’t want the user to be able to copy or assign instances of the class?************************

- with the example of an array class, you would have to use the following:

```cpp
//do not copy
Array( Array const &original ) = delete;

//do not assign
Array &operator=( Array const &righthand ) = delete;
```

- these go where you would have declared them normally in the class
- note that the thing to be copied must be passed in by reference

******************“this”****************** keyword

- refers to the current instance of the class
- carries the address of the object
    - which means *this is the object itself