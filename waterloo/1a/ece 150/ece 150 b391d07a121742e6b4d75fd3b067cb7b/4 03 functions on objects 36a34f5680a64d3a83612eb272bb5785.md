# 4.03 functions on objects

- we can explicitly tell a compiler to convert an integer to a double using static_cast<>
- C++ does not allow classes that you determine the size of at compile time
    - i.e. you can say an array is of size 50, or you could even dynamically allocate the array, but you cannot declare the size to be a non-definite value
    

```cpp
int main () {
	Array my_array{32, new double[32]{}};
		/*the array stored as a member for this instance of the 
			array class will be dynamically allocated
		*/

	for ( std::size_t k{0}; k < my_array.capacity_; ++k ) {
		my_array.array_[k] = 1.5;
	}

	//here, we can simply use the array 'my_array'

	delete[] my_array.array_; //telling the OS to deallocate the array
	my_array.array_ = nullptr; //since the member variable still has an 
														 //associated pointer, we want to give it 
														 //the null pointer
	my_array.capacity_ = 0; //to keep things consistent, we should reset capacity
```

***************overcoming functions being able to return just one value***************

- return a class that contains the values you want