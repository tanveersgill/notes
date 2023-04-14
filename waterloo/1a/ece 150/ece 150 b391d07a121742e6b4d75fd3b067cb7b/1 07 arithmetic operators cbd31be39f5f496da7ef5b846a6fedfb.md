# 1.07 arithmetic operators

- **binary arithmetic operator**
    - + , - , * , /
    - takes two operands and evaluates the operation between the two
    - for example, “+” is a binary arithmetic operator
- note that there is no operator for exponentiation
    - have to do something like x*x*x for x^3

- the left of an assignment operator has to be an assignment operator
    - you have to say x = something rather than like 2.0x + 23 = something
- **integer division**
    - the result of arithmetic operations on integers must produce an integer, including with division
    - the result is always just the quotient, and not any remainder
- **remainder of integer division**
    - use modulus operator
        - it gives the remainder of a division
- **standard conversions**
    - the conversion of literals by the compiler
    - whenever you have a binary operator, any ints get converted to doubles
    - if there are only integer operands, result is an int
        - if there is even one float, result will be a float
- **unary operators**
    - has only one operand
    - for example, ! is a unary operator
    
    there are two in C++:
    
    1. unary negation (-)
        1. it changes the sign of everything that follows
    2. neutral (+)
        1. leaves the sign unchanged