# 1.02 (program anatomy)

# notes on **program anatomy**

### **pre-processor directives**

- always start with a #
- **include directive (#include)**
    - tells us that a certain file should be included in compilation
    - basically, you are using someone else’s source code in your own
- **define directive (#define)**
    - will cover later

### statements

- can be
    - ***declaration*** of an ***identifier*** (name)
    - action being performed on data
- are always terminated with a semicolon

### block of statements

- anything surrounded by curly brackets
- they get executed in the order they appear, one at a time

### functions

- **declarations**
    
    tells the compiler:
    
    - name/identifier of the function
    - parameters of the function
    - return type of the function
- **example of a declaration**
    
    ```cpp
    int main();
    ```
    
- definitions
    
    like function declarations, but followed by a block of statements
    
- **example of a definition**
    
    ```cpp
    int main() {
    	std::cout << "hello world";
    	std::cout << std::endl
    
    return 0;
    }
    ```
    
    - everything inside the function is its body
    - when the function main is called, the body is executed
    

### main function

- if source code gets compiled into an executable, the first thing it does when it is run is call the main() function

### components of a function

1. literal data (numbers, characters, text, etc)
2. identifiers (names like main, return, std::cout)
3. operators (only way to manipulate data like +, ||, ≤, %)
4. delimiters