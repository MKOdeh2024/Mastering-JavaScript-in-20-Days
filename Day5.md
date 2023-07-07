
# Day 5: Data Fetching & Promises, Destructuring Data, Async and Modules


This README file explains some advanced concepts related to asynchronous Programming .

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- Data fetching is the process of retrieving data from an external source, typically over the internet. In JavaScript, this is commonly done using APIs (Application Programming Interfaces) provided by servers or third-party services. 
- Destructuring is a feature in JavaScript that allows you to extract values from arrays or properties from objects and assign them to variables in a more concise way.
- The async keyword is used in JavaScript to define asynchronous functions Which always returns a Promise, allowing you to use await inside the function to pause the execution until a Promise is resolved. 
-Modules in JavaScript are a way to organize code by splitting it into smaller, reusable pieces.

### Coding Example 
```javascript
// fetch Data 
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
// Destructing Data
const numbers = [1, 2, 3];
const [a, b, c] = numbers;

console.log(a); // 1
console.log(b); // 2
console.log(c); // 3

// Async
function fetchData() {
  return new Promise(resolve => {
    setTimeout(() => resolve('Data fetched!'), 1000);
  });
}

async function getData() {
  const data = await fetchData();
  console.log(data);
}

getData(); // It will log 'Data fetched!' after 1 second.

// modules
// math.js (module file)
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

// app.js (main file)
import { add, subtract } from './math.js';

console.log(add(2, 3));      // 5
console.log(subtract(5, 2)); // 3

```

## Coding Exercises

### [Build a Rick & Morty characters list](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week1-day5-task/task.md)
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

