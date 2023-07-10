
# Day 7: Async JavaScript and Promises

This README file explains important concepts in JavaScript that help manage asynchronous operations and make the code more readable and maintainable.

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- Asynchronous JavaScript allows you to perform tasks without blocking the execution of other code. 
- The **async** keyword is used to define an asynchronous function.
- The **await** keyword is used to pause the execution of an async function until a promise is resolved or rejected.
- Promises are objects that represent the eventual completion (or failure) of an asynchronous operation and its resulting value.
- Promises have two important methods:
1. **then()**: The **then()** method is used to handle the fulfilled state of a promise.
2. **catch()**: The **catch()** method is used to handle the rejected state of a promise. 
### Coding Example 
```javascript
function asyncOperation() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const result = Math.random();
      if (result > 0.5) {
        resolve(result);
      } else {
        reject('Error: Operation failed');
      }
    }, 2000);
  });
}

asyncOperation()
  .then(result => {
    console.log('Async operation succeeded with result:', result);
  })
  .catch(error => {
    console.log('Error:', error);
  });

```

## Coding Exercises

### [Exercises for Async JS & Promises](https://github.com/MKOdeh2024/week2-day3-tasks.git)
#### My Solution




