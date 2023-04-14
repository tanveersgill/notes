# 1.27 bitwise/bitshift operators (come back)

***bitwise***

- kind of like how we have boolean operators && / ||
    - but now its for bits (where 0 is false, 1 is true)

***AND ( & )***

- compares binary numbers bit-by-bit
- each resulting bit is 1 iff both bits are 1

***OR ( \ )***

- compares binary representations the same way as AND
- resulting bits are 0 iff both are 0

***XOR ( ^ )***

- resulting bit is 1 only if one bit is 1
- if both are the same, results in 0

***automatic bitwise assignment***

- &=, |=, and ^= are valid

***NOT ( ~ )***

- is unary
- applies the NOT operation to each bit
    - flips them
    

***bitshift operators*** 

- literally move bits left and right
- **x << n** shifts n bits to the left for any data type x
- **x >> n** shifts n bits to the right for x