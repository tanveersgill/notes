# 1.31 reference variables, pass-by-reference, and aliases

***alias in C++***

- one identifier is another name for a different identifier

```cpp
typename &newIdentifier{ existingIdentifier }
```

- its like declaring a new identifier and initializing it as another
- we are not making a new variable; instead we’re just making another name for the same variable

***pass-by-reference***

- when you prefix a parameter with &, it becomes an alias for the argument
- you can only pass values that can appear on the left of an assignment