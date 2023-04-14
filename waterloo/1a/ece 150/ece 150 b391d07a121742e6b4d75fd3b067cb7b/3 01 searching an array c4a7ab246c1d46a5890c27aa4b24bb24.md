# 3.01 searching an array

if we want to determine if an array contains a specific value, we can search 

- we might want to pass in all values as const

************linear search************

- can go through the array and return true if it is found
- but what if we want the actual index where it is found?
    - could pass an index variable by reference, and update it with the index
    - or, we could return the index if found, and if it isn’t found, return some special value