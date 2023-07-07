
# Day 6: JavaScript Principles (Functions & Callbacks) 


This README file explains some advanced concepts related to Functions  .

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- JavaScript is single-threaded, meaning it executes one statement at a time in a sequential manner.
- Execution Stack (Call Stack): JavaScript uses an execution stack, also known as the call stack, to manage the order of function calls and track their execution contexts.
- callback function is a function that is passed as an argument to another function and is invoked or called when a certain event or condition occurs.
-Higher-order functions are functions that can take other functions as arguments or return functions as their results.
-Arrow functions were introduced in ES6 which allow us to write shorter function syntax.
-Pair programming is a software development practice in which two programmers work collaboratively on the same task or piece of code.
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

### [Build a Rick & Morty characters list]()
#### My Solution


```javascript
// script.js
async function fetchAliveCharacters() {
  try {
    const response = await fetch(
      "https://rickandmortyapi.com/api/character?status=alive"
    );
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }

    const data = await response.json();
    return data.results.slice(0, 50);
  } catch (error) {
    console.error("Error fetching data:", error);
    throw error;
  }
}

async function displayAliveCharacters() {
  try {
    const characterList = document.getElementById("characterList");
    const characters = await fetchAliveCharacters();

    characters.forEach((character) => {
      const li = document.createElement("li");
      li.innerHTML = `
        <h3>${character.name}</h3>
        <img src="${character.image}" alt="${character.name}">
        <p>Location: ${character.location.name}</p>
        <p>Species: ${character.species}</p>
        <p>Gender: ${character.gender}</p>
      `;
      characterList.appendChild(li);
    });
  } catch (error) {
    const characterList = document.getElementById("character-list");
    characterList.innerHTML =
      "<p>Error fetching characters. Please try again later.</p>";
    console.error("Error:", error);
  }
}

displayAliveCharacters();

```

