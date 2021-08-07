 # Hoisting in Javascript  

JavaScript Hoisting refers to the process whereby the compiler allocates memory for variable and function declarations prior to execution of the code. 

Declarations that are made using var are initialized with a default value of undefined. Declarations made using let and const are not initialized as part of hoisting.

JavaScript only hoists declarations, not initializations. 

If a variable is used in code and then declared and initialized, the value when it is used will be its default initialization (undefined for a variable declared using var, otherwise uninitialized). 

**For example:**
```
console.log(num); // Returns 'undefined' from hoisted var declaration (not 6)
var num; // Declaration
num = 6; // Initialization
```
> The example below only has initialization. No hoisting happens so trying to read the variable results in ReferenceError exception.
```
console.log(num); // Throws ReferenceError exception
num = 6; // Initialization
```
