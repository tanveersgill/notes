# 4.04 operator overloading

- essentially defining operations between classes such as addition (+) or negation (-)

- say we have two instances of the Rational class, and we want to ‘add’ the two.
    - then, we can define our own overloaded operator so that whenever the compiler sees *********************Rational + Rational,********************* it will do what is in that function
    - of course, the operator is defined in the form of a function
    
    ```cpp
    Rational operator+( Rational const &p, Rational const &q );
    ```
    
- almost every operator can be overloaded to do things other than its original purpose
    - like !=, ==, +, -, etc

*********************************what not to overload*********************************

- this will just make sense to you
    - things like division for vectors don’t exist, so you wouldn’t want to overload the / operator for a vector class