
# Day 10: Classes & Prototypes & Wrapping up

This README file explains Types  and Coercion in js.

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- Classes are a blueprint or template for creating objects.
- They encapsulate data (attributes) and operations (methods) that define the behavior and characteristics of objects. 
- classes allow you to create multiple and independent instances (objects) based on the same blueprint.
- Prototypes provide a mechanism for objects to inherit properties and methods from other objects.
- In JavaScript, every object has an internal property called [[Prototype]], which references another object or **null**.
- When you access a property or call a method on an object, and the property or method is not found directly on the object itself, JavaScript automatically looks for it in the object's prototype.
- wrapping up typically refers to encapsulating code within a function or module to create a closure and control the scope of variables and functions.
### Coding Example 
```javascript
// Wrapping up code in a module
const myModule = (function() {
  // Private variable
  let privateVar = 'Private variable';

  // Private function
  function privateFunc() {
    console.log('Private function');
  }

  // Class definition using ES6 class syntax
  class MyClass {
    constructor(name) {
      this.name = name;
    }

    // Prototype method
    greet() {
      console.log(`Hello, my name is ${this.name}`);
    }
  }

  // Public API
  return {
    // Public method
    publicMethod: function() {
      console.log('Public method');
    },

    // Creating instances of MyClass
    createInstance: function(name) {
      return new MyClass(name);
    },

    // Accessing private variable
    getPrivateVar: function() {
      return privateVar;
    }
  };
})();

myModule.publicMethod();  // Output: Public method

const instance = myModule.createInstance('Alice');
instance.greet();         // Output: Hello, my name is Alice

console.log(myModule.getPrivateVar());   // Output: Private variable

```

## Coding Exercises

### [Object Oriented Programming in FreeCodeCamp.](https://www.freecodecamp.org/fcce5aa636f-0382-4e96-a0d3-f54c7866d398)
#### Click on the title to reach to solution
