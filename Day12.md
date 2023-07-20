
# Day 12: Advanced Scope & Function Expressions

Advanced scope and function expressions refer to the more complex and sophisticated features related to the scope and behavior of functions in JS.
## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- **Function expression** is a way to define a function using an expression instead of a function declaration.
- A **Named Function expression** is an example of function expressions allows you to assign a name to the function, which can be useful for self-referencing or debugging purposes.
- **Arrow functions**, introduced in ECMAScript 6 (ES6), provide a more concise syntax for defining functions in JavaScript.
- Here's a hierarchy of function types in JavaScript : Function Declarations, Function Expressions, Arrow Functions, Higher-Order Functions, Anonymous Functions
IIFE (Immediately Invoked Function Expression)
- **Lexical** scope means that the scope of a variable is determined by its position in the source code during the lexing phase
-  That means the scope is fixed and defined by where the variables and functions are declared physically in the code.
- **Dynamic** scope, unlike lexical scope, determines the scope of a variable based on the flow of execution during runtime (not applicable inJS).
- Scope defines the accessibility and visibility of variables in JavaScript. 
- **Function** scope refers to the concept that variables declared within a function are only accessible within that function and its nested functions, creating a local scope for those variables.
- JAn **IIFE** (Immediately Invoked Function Expression) is a JavaScript design pattern used to create a private scope for variables and prevent them from polluting the global namespace. 
- It involves defining a function expression and immediately invoking it, encapsulating the code within its scope. 
- The primary purpose of an IIFE is to provide a way to execute code immediately without leaving any variables or function declarations in the global scope.
- **Block** scoping in JavaScript is a way to declare variables that are confined to the block in which they are defined.
- **Let** is a block scope while **var** is a function scope.
### Coding Example 
```javascript
// 1. Function Declaration
function greet(name) {
  return `Hello, ${name}!`;
}

// 2. Function Expression
const add = function(a, b) {
  return a + b;
};

// 3. Arrow Function
const subtract = (a, b) => a - b;

// 4. Higher-Order Function
function applyOperation(operation, a, b) {
  return operation(a, b);
}

// 5. Anonymous Function (used as a callback)
setTimeout(function() {
  console.log('This is an anonymous function used as a callback.');
}, 1000);

// 6. IIFE (Immediately Invoked Function Expression)
(function() {
  console.log('This is an IIFE.');
})();

// Lexical scope
function outer() {
  const x = 10;
  function inner() {
    console.log(x); // inner function can access 'x' from the outer function's scope
  }
  inner();
}
outer(); // Output: 10

function outer() {
  const x = 10;
  function inner() {
    console.log(x); // If JavaScript used dynamic scope, this would look for 'x' in the scope of the caller, not the lexical scope.
  }
  inner();
}
outer();



```

## Coding Exercises

### [SECTION'S EXERCISES](https://github.com/MKOdeh2024/week3-day2-tasks.git)
#### Click on the title to reach to solution
