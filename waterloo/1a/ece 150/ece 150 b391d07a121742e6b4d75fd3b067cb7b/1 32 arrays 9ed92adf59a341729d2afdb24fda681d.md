# 1.32 arrays

***declaring***:

```cpp
typename name[size]{};
```

- where size is 0 or positive
- here, the values all get default values

Given the above declaration, the compiler will allocate as many consecutive bytes as needed to store the n variables

***initializing***:

```cpp
typename name[size]{entry 1, entry 2, ... , entry size}
```

- you can pass in less than size entries, the extras will get default values

***exceeding array bounds:***

- C++ just goes to the corresponding location in memory that would have existed if the array was the right size
    
    ![Screen Shot 2022-10-10 at 3.32.02 PM.png](1%2032%20arrays%209ed92adf59a341729d2afdb24fda681d/Screen_Shot_2022-10-10_at_3.32.02_PM.png)