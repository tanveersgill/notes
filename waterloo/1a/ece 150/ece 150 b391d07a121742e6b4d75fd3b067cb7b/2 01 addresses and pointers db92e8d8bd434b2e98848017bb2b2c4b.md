# 2.01 addresses and pointers

- every single byte has an address
    - these addresses are represented in hexadecimal
- 64-bit processors are able to store 2^64 different addresses
    - so essentially, address sizes are fixed based on the processor
- we can store addresses in variables, and also indicate the type of variable that is being stored in the address

******************************for arrays******************************

```cpp
int grrBow[10];

int *addressName{grrBow};
```

the asterisk indicates that the identifier following it is the address of something (a double or int)

- note that for arrays, the name stores the address of the first byte

************************************for variables************************************

- need to use the unary address operator, &

```cpp
double a{};

std::cout << &a << std::endl;
```

- just like we did with arrays, we can assign addresses of local variables to other variables

```cpp
double a{};

double *addressOfA{ $a };
```

************************pointers************************

- variables that store addresses are called
- we should prefix pointers with “p_”
    - don’t *****have***** to, but it is a practice in industry

```cpp
int ape {44}
int *p_monkey{&ape};

std::cout << p_monkey << std::endl;
std::cout << *p_monkey << std::endl;
```

- you can also update the value that is at a certain address using the address variable

```cpp
*p_monkey = 69;
```

***************************std::size_t***************************

- if a local variable will be used to index an array, it will be of type std::size_t
    - this type is guaranteed to store the max index for a given processor