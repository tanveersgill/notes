# 1.28 floating point primitive data types

- double and floats store approximations of real numbers

***what is the precision?***

- the number of decimal digits used

- if the exponent is too large, the number cannot be stored

***weaknesses of fixed precision***

- associativity does not work
    - (x+y) + z doesn’t equal (x + z) + y
- x-y might not work if x is almost y

cannot use %, bitwise, or bitshift operators with floating point numbers