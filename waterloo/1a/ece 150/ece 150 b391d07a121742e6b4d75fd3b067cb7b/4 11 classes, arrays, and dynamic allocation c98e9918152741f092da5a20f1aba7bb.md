# 4.11 classes, arrays, and dynamic allocation

************************************************************************************passing arrays to functions************************************************************************************

- recall that when we pass an array to a function, its address is what’s getting passed in.
    - this means that no copy is made, and we don’t have to worry about copying
        - in a sense, it is kind of like passing by reference

*****************dynamic allocation of objects*****************

- just as we’d expect
    - remember with an integer, we could do new int{} for a dynamically allocated integer with the default value 0
    - or we could do new int{65} for a dynamically allocated integer with value 65
- for a class:
    - just say new ClassName{}
    - in the curly braces, you may pass in values to initialize the object with
        - note that this will return the pointer to the dynamically allocated item
        - constructor will get called right after the memory is allocated
    - **************MUST CALL DELETE ON THE ADDRESS, OR THE MEMORY IS NOT DEALLOCATED**************
        - when we do this, it calls the destructor on the object at the dynamically allocated address.

***************************************************************accessing member variables/functions on pointers to instances of classes***************************************************************

- we have to use “→” instead of “.”
    - for example, consider the following code:
    
    ```cpp
    int main () {
    	Monkey ape{ 69 };
    	Monkey *p_gorilla{ new Monkey { 420 } };
    
    	ape.getNum(); 
    		//this goes thru the 
    		//member function of the instance ape
    	p_gorilla -> getNum();
    		//this goes thru the member function
    		//for the dynamically allocated Monkey instance
    		//that p_gorilla points to
    
    }
    ```
    

************************a quick rule:************************

- if printing a variable produces an address, you should realize that that is actually a pointer, and you should use the arrow operator
    - will help to prefix pointer names with a p_
    - prefix dynamically allocated arrays with a_