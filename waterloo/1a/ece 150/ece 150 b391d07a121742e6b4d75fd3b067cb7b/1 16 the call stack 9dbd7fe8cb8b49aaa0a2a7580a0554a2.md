# 1.16 the call stack

- ***what happens when a program is run?***
    - it gets converted into a sequence of instructions the computer can execute
        - these instructions (”executables”) then get stored within a file, which is in a file system
        - each instruction has its own address
        
    - the instructions and constants get loaded into main memory
        - this main memory is volatile, disappearing when the computer is off. it is able to access values much faster than persistent memory
    - then, the processor executes one instruction at a time

- ***where are local variables stored***
    - at the bottom of main memory
    - this is what we call the call stack

- ***three sections of main memory***
    1. instructions
    2. constants
    3. local variables (call stack)