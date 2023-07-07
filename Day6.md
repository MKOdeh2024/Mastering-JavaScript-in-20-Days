
# Day 6: JavaScript Principles (Functions & Callbacks) 


This README file explains some advanced concepts related to Functions  .

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- JavaScript is single-threaded, meaning it executes one statement at a time in a sequential manner.
- Execution Stack (Call Stack): JavaScript uses an execution stack, also known as the call stack, to manage the order of function calls and track their execution contexts.
- callback function is a function that is passed as an argument to another function and is invoked or called when a certain event or condition occurs.
- Higher-order functions are functions that can take other functions as arguments or return functions as their results.
- Arrow functions were introduced in ES6 which allow us to write shorter function syntax.
- Pair programming is a software development practice in which two programmers work collaboratively on the same task or piece of code.
### Coding Example 
```javascript
// Higher-order function that takes a callback function as an argument
function higherOrderFunction(callback) {
  // Perform some operation
  const result = callback(10, 20);
  console.log("Result:", result);
}

// Callback function to be passed to the higher-order function
const callbackFunction = (a, b) => a + b;

// Calling the higher-order function with the callback function
higherOrderFunction(callbackFunction);

```

## Coding Exercises

### [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)
#### My Solution


```javascript
const squareList = arr => {
   
  return arr.filter(item => item >=0 && Number.isInteger(item)).map(item => item * item);
  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);

```

## Coding Exercises

### [Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)
#### My Solution


```javascript
// Only change code below this line
function urlSlug(title) {
// Convert title to lowercase and split into an array of words
  const words = title.toLowerCase().trim().split(/\s+/);
  
  // Join the words with hyphens to create the slug
  const slug = words.join('-');
  
  return slug;
}
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");
```
## Coding Exercises

### [Exercises for functions and callbacks](https://github.com/MKOdeh2024/week2-day1-tasks.git)
#### My Solution



