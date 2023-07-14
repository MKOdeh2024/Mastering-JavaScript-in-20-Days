
# Day 10: Classes & Prototypes & Wrapping up

This README file explains Types  and Coercion in js.

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- primitive types are data types that are not objects and do not have methods or properties. Tey are ımmutable 
- **undefined** refers to a special value that represents the absence of a value or the uninitialized state of a variable. It is assigned to variables that have been declared but not assigned a value.
- **Undeclared** variables, on the other hand, are variables that have not been declared using the var, let, or const keywords. Accessing an undeclared variable will result in a ReferenceError.
- **NaN** (invalid Number) is a special value that represents the result of an invalid or undefined mathematical operation.
- The **isNaN()** function is used to determine whether a value is NaN or not. 
- Negative zero (-0) is a special case that behaves differently from regular zero (0) in certain operations.
- Coercion in JavaScript refers to the automatic conversion of values from one type to another by the JavaScript engine.
- JavaScript has two types of coercion: implicit coercion and explicit coercion.
- Abstract operations are internal operations defined by the language specification that dictate how various operations are performed on values.
### Coding Example 
```javascript
let num = 42;         // Number
let str = "Hello";    // String
let bool = true;      // Boolean
let undef = undefined;// Undefined
let n = null;         // Null
let sym = Symbol();   // Symbol
let x; // variable declared but not assigned a value
console.log(x); // Output: undefined
console.log(y); // ReferenceError: y is not defined
let result = 0 / 0; // Performing an invalid division
console.log(result); // Output: NaN

console.log(isNaN(result)); // Output: true
console.log(isNaN(42)); // Output: false
// Negative Zero
console.log(1 / 0);   // Output: Infinity
console.log(1 / -0);  // Output: -Infinity

console.log(-0 === 0);            // Output: true
console.log(-0 === 0 && 1 / -0);  // Output: false

// Implicit corecion
let num = 42;              // Number
let str = "The answer is "; // String

let result = str + num;
console.log(result);  // Output: "The answer is 42"

// Explicit coercion to Number type
let numStr = "42";       // String
let num = Number(numStr); 

console.log(num);  // Output: 42

```

## Coding Exercises

### [TYPES AND COERCION EXERCISES](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)
#### Click on the title to reach to solution
