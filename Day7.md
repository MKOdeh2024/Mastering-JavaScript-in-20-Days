
# Day 7: Clousers 


This README file explains a powerful concept called  Clousers.

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- In JavaScript, closures are a powerful concept that allows functions to remember and access variables from the scope in which they were defined, even if that scope has finished executing.
- Closures are created when a function is defined inside another function and the inner function retains access to the variables and parameters of the outer function.
- Closures allow you to create private variables or encapsulated data.
- Closures are useful for creating functions with persistent state.  
### Coding Example 
```javascript
function outerFunction() {
  var outerVariable = 'I am from the outer function';

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

var closure = outerFunction();
closure();  // Outputs: I am from the outer function

```

## Coding Exercises

### [Exercises for closures](https://github.com/MKOdeh2024/week2-day2-tasks.git)
#### My Solution


```javascript

```

