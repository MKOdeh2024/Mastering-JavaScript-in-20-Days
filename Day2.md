
# Day 2: Basic Javascript and Data structure

This README file summarizes the JavaScript basics and talks about some data structure like Arrays and Objects.

## Lesson Summary

In this lesson, we explored some concepts in JavaScript. Here are the key points covered:

- Expressions are combinations of values, variables, operators, and function calls that produce a result (ex: "5 + 10"). 
- Arrays are ordered collections of elements stored under a single variable name and can hold various data types.
- Objects are complex data structures consisting of key-value pairs, where each key is a property and its corresponding value can be of any data type.
## Coding Examples

```javascript
// Expressions
let a = 5;
let b = 10;
let sum = a + b; // Addition expression
console.log('Sum:', sum);

// Arrays
let fruits = ['Apple', 'Banana', 'Orange'];
console.log('Fruits:', fruits);

let numbers = [1, 2, 3, 4, 5];
console.log('Numbers:', numbers);

console.log('Length of fruits array:', fruits.length);

// Objects
let person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    isEmployed: true,
    hobbies: ['Reading', 'Coding', 'Painting']
};

console.log('Person object:', person);

```


## Coding Exercises

### [Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)
#### My Solution


```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
// Search for the contact by name
  const contact = contacts.find((c) => c.firstName === name);

  // If contact not found, return "No such contact"
  if (!contact) {
    return "No such contact";
  }

  // Check if the property exists in the contact
  if (contact.hasOwnProperty(prop)) {
    return contact[prop]; // Return the value of the property
  } else {
    return "No such property"; // Property not found in the contact
  }
  // Only change code above this line
}

lookUpProfile("Akira", "likes");
```

### [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)
#### My Solution


```javascript
function forecast(arr) {
  // Only change code below this line

  return arr.slice(arr.indexOf('warm'), arr.indexOf('sunny') +1);
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

### [Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)
#### My Solution


```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment, 'is', 'fun']
  return sentence;
}

console.log(spreadOut());
```

