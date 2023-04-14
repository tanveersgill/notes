# 4.01 class data structures

- if we have a bunch of local variables that are closely related, like information on an object such as its size dimensions and mass, classes allow us to group this information together

```cpp
class Body {
	public:
		//member variables
		double position_[3];
		double velocity_[3];
		double mass_;
}
```

- classes refer to types, just as int and double do
- this means we can declare local variables to be instances of a class
    - like if the class represents students, we can make a variable called “studentOne” that contains information on a specific student

******************************************************class declarations******************************************************

- found at the top of your code

```cpp
class Body;

int main();
```

*********class definitions*********

- the actual code for the class itself

***************class initialization***************

- treat it like initializing any other local variable, except now you have to pass in the values for each of the member variables
- member variables are initialized in the order in which they appear
    - using the example of the Body class from above, if we wanted to make an instance of the class for the planet Earth, we could initialize it like this in main:
    
    ```cpp
    int main () {
    	Body earth { {149.6e6 , 0.0 , 0.0} , {0.0 , 107e3 , 0.0} , 5.972e24}
    }
    ```
    

***************accessing member variables***************

- use the “ . “ operator
    - for example,
    
    ```cpp
    std::cout << earth.mass_ << std::endl;
    std::cout << earth.position_[0] << std.endl;
    ```
    

***************************************************************************************manipulating member variables***************************************************************************************

- also use the . operator, and just update shit like its a normal local variable
    - example:
    
    ```cpp
    earth.position_[0] += 1;
    ```
    

******************************can you initialize an instance with the values from another class?******************************

- yes, just treat it like a normal local variable again
    - say we wanted a temporary instance of Body with the same stuff as the instance ‘earth’ in it:
    
    ```cpp
    Body tmp { earth };
    //or
    Body tmp = earth;
    ```
    

************************************************************************************can you pass objects in as arguments to a function?************************************************************************************

- yes.
    
    ```cpp
    double thisIsAMethod ( Body odyShapeLikeCola );
    
    double thisIsAMethodThatReturnsTheMass ( Body odyShapeLikeCola ) {
    	return odyShapeLikeCola.mass;
    }
    ```
    
- how does this look in the call stack? :
    - when you call the function, memory is reserved for the parameter, and information is copied over

******************************************************************why pass by reference?******************************************************************

- so we avoid copying over large amounts of information every time we need to create a local variable