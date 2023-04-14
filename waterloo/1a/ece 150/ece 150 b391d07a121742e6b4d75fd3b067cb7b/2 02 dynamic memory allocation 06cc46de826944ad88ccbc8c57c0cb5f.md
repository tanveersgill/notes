# 2.02 dynamic memory allocation

**************revisiting *******static******* memory allocation**

- all the memory we’ve dealt with so far
    - parameters/local variables
- in this case, the memory is allocated on the call stack and gets deleted when functions are returned

**************************************************dynamic memory allocation**************************************************

- why?
    - what if we don’t know beforehand how much memory our program needs?
    - as it goes on, we might need to keep on allocating memory, so how do we do that?
- the operating system deals with memory management, so if you want memory you have to make a request to the OS

****************the heap****************

- found between the call stack and instructions/constants
- this is the memory used for dynamically allocated memory
    
    ************how it works************
    
    - the operating system looks for x bytes of memory in the heap that isn’t being used by some other program
    - it then flags the memory as allocated to your program
    
    *********************************************how we get the dynamically allocated memory*********************************************
    
    - the operating system returns an address, and we just have to assign it to a pointer

************new**** operator**

- unary operator
- its operand is a type (ex. int)
- it requests enough memory from the operating system for the specified type, and returns the supplied address

```cpp
int main () {
	int *p_int{};
	
	p_int = new int{ 42 };

	return 0;
}
```

- note for the above:
    - if we want to access what is at the new memory, we use *p_int because p_int itself carries the address
    

*********************delete******* operator**

- just like programs can request memory, they can also tell the OS that they don’t need that memory anymore, or to deallocate it

adding on to the previous example:

```cpp
int main () {
	int *p_int{};
	
	p_int = new int{ 42 };

	delete p_int; //address stored is sent to the OS, and the OS flags the memory as deallocated
	
	p_int = nullptr; //since the address is still assigned to p_int, we set it to nullptr

	return 0;
}
```

******************nullptr:****************** 

- simply stores the zero address

note that even after we use delete, p_int still stores the address.