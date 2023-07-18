
# Day 11: Static Typing and Scope

Tstatic typing and scope are two important concepts that affect how variables are defined and used in the language.

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- JavaScript is primarily a dynamically typed language, which means that variable types are determined at runtime.
- However, there are tools and extensions available, such as TypeScript and Flow, that introduce static typing to JavaScript.
- *Static typing allows you to define the types of variables explicitly. 
- Scope defines the accessibility and visibility of variables in JavaScript. 
- Variables declared in different scopes have different lifetimes and can be accessed from different parts of the code.
- NJavaScript has two main types of scope: global scope and function scope.
- **Global Scope:** Variables declared outside any function have global scope.
- Global variables can be accessed and modified by any part of the code, which can lead to potential naming conflicts or unintended modifications.
- Function Scope: Variables declared inside a function have function scope. They are accessible only within the function block and any nested functions.
- Function scope helps encapsulate variables and avoid naming conflicts with variables in other functions.
### Coding Example 
```javascript
let age: number = 25; // static typing
let globalVariable = "I'm a global variable";

function foo() {
let functionVariable = "I'm a function variable";
  console.log(functionVariable); // Accessible within the function
  console.log(globalVariable); // Accessible from within the function
}

foo();
console.log(functionVariable); // Error: functionVariable is not defined
if (true) {
  let blockVariable = "I'm a block variable";
  console.log(blockVariable); // Accessible within the block
}

console.log(blockVariable); // Error: blockVariable is not defined


```

## Coding Exercises

### [SECTION'S EXERCISES](https://github.com/MKOdeh2024/week3-day2-tasks.git)
#### Click on the title to reach to solution

