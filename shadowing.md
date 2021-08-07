   # Variable Shadowing  

**What is ‘variable shadowing'?**

Variable shadowing occurs when a variable of an inner scope is defined with the same name as a variable in the outer scope. 

In the inner scope, both variables’ scope overlap. According to variable scoping rules, the inner scope should always be able to access a variable defined in the outer scope

But in practice, shadowing will prevent that from happening

**Example 1 :**
```
let points = 10;

function displayDouble() {
  let number = 2;
  number = points * number; // variable 'points' is accessible in the inner scope
  console.log(number); //=> 20
}

displayDouble();
```
>In this first example, each variable is distinctly named and we can see that variable points initialised before defining the function in the outer scope and is accessible in the inner scope of function .displayDouble() 

**Example 2 :** 
```
let number = 10;

function displayDouble() {
  //a new variable is defined with the same name as variable on line 26 - outer scope
  let number = 3;

  number *= 2;
  console.log(number); //=> 6
} 


displayDouble();
console.log(number); //=> 10
```

>we saw that variable shadowing can occur in methods or functions —such as .displayDouble() where the global variable 'number' is shadowed by the inner variable of the same name inside the block of function displayDouble().

