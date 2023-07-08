
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

### [Exercises for closures](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md)
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



