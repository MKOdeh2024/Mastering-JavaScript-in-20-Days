
# Day 4: Functional Programming

This README file explains some concepts of a parogramming paradigm called Functional Programming .

## Lesson Summary

In this lesson, we learned some convepts and solved  some excersies in JavaScript. Here are the key points covered:

- Event handlers are functions that are executed when a specific event occurs. They are used to respond to user interactions and trigger specific actions accordingly.
- Conditionals in JavaScript are used to make decisions based on different conditions. The most common conditional statements are if, else if, and else.
-map(): It creates a new array by applying a callback function to each element of the original array.
-filter(): It creates a new array with all elements that pass a given condition (determined by a callback function).

### Coding Example 
```javascript
// Event handler
const button = document.getElementById('myButton');
button.addEventListener('click', function() {
  alert('Button clicked!');
});

const num = 10;

if (num > 0) {
  console.log('The number is positive.');
} else if (num < 0) {
  console.log('The number is negative.');
} else {
  console.log('The number is zero.');
}
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.map(num => num * 2);
const evenNumbers = numbers.filter(num => num % 2 === 0);

console.log(evenNumbers); // Output: [2, 4]
console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]

}
```

## Coding Exercises

### [Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)
#### My Solution


```javascript
function checkSign(num) {
return num >0 ? "positive" : num <0 ? "negative" : "zero";
}

checkSign(10);
```

### [Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)
#### My Solution


```javascript
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
  if(strokes === 1)
  return "Hole-in-one!";
  else if(strokes <= par -2)
  return "Eagle";
  else if(strokes === par - 1)
  return "Birdie";
else if(strokes === par )
  return "Par";
  else if(strokes === par + 1)
  return "Bogey";
  else if(strokes === par + 2)
  return "Double Bogey";
  else if(strokes >= par +3 )
  return "Go Home!";

else 
  return "Change Me";
  // Only change code above this line
}

golfScore(5, 4);
```

### [Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)
#### My Solution


```javascript
const ratings = watchList.map(movie => ({
  "title": movie["Title"],
  "rating": movie["imdbRating"]
}));


// Only change code above this line

console.log(JSON.stringify(ratings));
```

### [Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)
#### My Solution


```javascript
const filteredList = watchList.filter(movie => parseFloat(movie["imdbRating"]) >= 8.0).map(movie => ({
    "title": movie["Title"],
    "rating": movie["imdbRating"]
  }));
// Only change code above this line

console.log(filteredList);
```

