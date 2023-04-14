# 1.06 initialization of and assignment to local variables

- **previously:**
    - we declared a local variable
        - meaning we specified its type and identifier (name)
        - we then gave it a value through user input
- **what happens if you just declare an identifier to be a local variable?**
    
    ```cpp
    int n;
    ```
    
    - it gets a random value
        - because local variables are stored in main memory; whatever is already there gets assigned
    
- **how can you give it a default value?**
    
    ```cpp
    int n{};
    ```
    
    - note that for int, double, and booleans, this default is 0.
    - for char, it is the null character
    
- **what is meant by initializing**
    - to give a value

this is valid by the way:

```cpp
int n{};
int m{};

m = n = 10;
```

- both m and n are assigned the value 10