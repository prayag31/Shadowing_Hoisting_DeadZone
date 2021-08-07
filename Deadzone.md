 # Temporal dead zone (TDZ)    


Let variables cannot be read/written until they have been fully initialized, which happens when they are declared (if no initial value is specified on declaration, the variable is initialized with a value of `undefined`). 

Accessing the variable before the initialization results in a `ReferenceError`. 

This differs from var variables, which will return a value of undefined if they are accessed before they are declared.

The variable is said to be in a "_**temporal dead zone_**" (TDZ) from the start of the block until the initialization has completed.


 **For example :** 
```
{ // TDZ starts at beginning of scope
    console.log(bar); // undefined
    console.log(foo); // ReferenceError
    var bar = 1;
    let foo = 2; // End of TDZ (for foo)
  }```
