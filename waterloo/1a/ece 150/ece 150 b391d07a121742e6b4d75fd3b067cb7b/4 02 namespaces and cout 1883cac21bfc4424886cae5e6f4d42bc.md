# 4.02 namespaces and cout

- we have been using the std namespace thus far
- say you have some functions that you don’t want to be used unless actually intended.
    - then, you can wrap them in a namespace, so that they can be used when needed
    
    ```cpp
    namespace tanveer {
    	double monkey ();
    
    	double monkey () {
    		//this function does something
    	}
    }
    
    int main () {
    	monkey(); //THIS WON'T WORK!
    	
    	tanveer::monkey(); //VALID, WE NAMED THE NAMESPACE
    }
    ```
    
- keep in mind, there is nothing special about the standard namespace.
    - if you wanted, you could just add your own variables, functions, and classes to it
- you can also have namespaces within namespaces
    - like if you had a company, you might need a company-wide namespace, and then one within that for a specific project