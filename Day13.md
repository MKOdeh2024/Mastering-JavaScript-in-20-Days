
# Day 13: Advanced Scope & Closure

This file explains the remained Advanced scope concepts and closure.
## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- **Hoisting** is a JavaScript mechanism where variable and function declarations are moved to the top of their containing scope during the compilation phase before the code is executed. 
- **Const** keyward is used with variables to prevent reassigning it (promitives) but an element of array of conatant can be reassigned 
- Variables declared with **var** are hoisted and initialized with undefined.
- Variables declared with **let** and **const** are hoisted but not initialized, and accessing them before the actual declaration results in a ReferenceError.
- Function declarations are hoisted and can be called before their actual declaration.
- A **closure** is formed when an inner function is defined within the lexical scope of an outer function. 
-  The main purpose of closure is encapsulating variables or functions in the outer function.
- The **Module Pattern** is a design pattern in JavaScript used to create encapsulated and reusable code by leveraging closures and immediately-invoked function expressions (IIFE). 
- Here's how to implement the Module Pattern:
1. Create an IIFE: Wrap the module code in an immediately-invoked function expression.
   This helps to create a private scope for the module, preventing pollution of the global namespace.
2. Define private members: Within the IIFE, define variables and functions that should be private and not directly accessible from outside the module.
3. Return an object (the public interface): From the IIFE, return an object that exposes the public members of the module. These are the methods or properties that you want to make accessible from outside the module, providing a controlled interface to interact with the module. 

### Coding Example 
```javascript
// Module Pattern with Hoisting and Closure
const calculatorModule = (function() {
  // Private variables
  var x = 0;
  var y = 0;

  // Private function
  function add() {
    return x + y;
  }

  // Public interface (returned object)
  return {
    setX: function(value) {
      x = value;
    },
    setY: function(value) {
      y = value;
    },
    getResult: function() {
      return add();
    }
  };
})();

// Using the calculator module
calculatorModule.setX(5);
calculatorModule.setY(3);
console.log(calculatorModule.getResult()); // Output: 8

```

## Coding Exercises

### [SECTION'S EXERCISES](https://github.com/MKOdeh2024/week3-day3-tasks.git)
#### Click on the title to reach to solution
