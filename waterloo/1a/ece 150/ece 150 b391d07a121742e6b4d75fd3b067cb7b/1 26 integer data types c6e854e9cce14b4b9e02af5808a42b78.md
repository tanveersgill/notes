# 1.26 integer data types

- All of main memory is divided into bytes
    - A grouping of 8 bits
- Note: if we have a set number of decimal digits *n,* we can store 10^n values
- If we have *n* bits (binary digits), we can store 2^n values
    - all zeroes to all ones

- ***how is int stored on the computer?***
    - every local variable int takes up 32 bits
    - somewhere in main memory, 32 back-to-back bits are allocated to store the int
        - when we try to print the number, cout interprets those bits as an integer

- ***how to store negative numbers? (2s compliment)***
    - take the positive value and flip all of its bits
        - then add one
    - easier way:
        - flip all bits up to but not including the right-most 1
    - leading bit tells us the sign (1 means negative)

- ***unsigned int***
    - all 32 bits of unsigned int get used to store positive integers
    - use when you never need negative numbers

- ***other int types:***
    - unsigned short → 16 bits/2 bytes
    - unsigned long → 64 bits/8 bytes
    - unsigned char → 8 bits/1byte (ASCII)

- ***what happens when you go over the limit of a type (a carry)***
    - for example, if you use unsigned short to add two shorts, but their result does not fit in a short
    
    → basically, the operation is done in binary, and then all bits past the limit are dropped (for ***short***, this was 16 bits)
    

- ***signed arithmetic***
    - for addition, just treat it as though you only have unsigned values (++ remember to limit based on size)
    - with subtraction, take the 2s compliment of the second number and add to the first