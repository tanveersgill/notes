# 1.30 default parameter values

- specified in the function declaration with normal assignment operators

- when a function is called, the kth argument gets matched with the kth parameter.
    - So, if you decide to pass in less than k parameters, ensure that you’ve entered at least those without default values
        - Otherwise, it won’t compile
    - anything leftover will take on its default value