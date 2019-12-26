---
title: "Javascript Array Map"
date: 2019-12-26
categories:
  - Code
tags:
  - basics
  - javascript
  - ES6
header:
    #teaser: /assets/images/2019-09-18/header.png
    #image: /assets/images/2019-09-18/header.png
    #og_image: /assets/images/2019-09-18/header.png
published: true
---

## Javascript Array Map
Javascript ES6 gave us .map(), a function that works the same as a traditional for loop but with benefits. So what's different?

### Multiplying by two
Let's say we want to loop over an array of numbers and multiply them by 2. Here's our array: 

```javascript
const data = [4, 8, 15, 16, 32, 42];
```

How would we multiply each number? A traditional for loop would look like this:

```javascript
function multiplyByTwo(arr) {
  let newArr = []; // We create an empty array for future storage

  for (let i = 0; i < arr.length; i++) { // Looping through the given array (const data), iterating through each item
    newArr.push(arr[i] * 2); // Each iteration gets multiplied by two and pushed into the empty array
  }

  return newArr; // Returning the array that now contains the new items pushed into it in the for loop
}

console.log(multiplyByTwo(data)); // Calling our function with the data array
```

Using map, there's no need for a for loop as map does the looping for us. This shortens the code:

```javascript
function multiplyByTwo(arr) {
  return arr.map(function(num) { 
    return num * 2;
  })
}

console.log(multiplyByTwo(data));
```

ES6 gives us further shorthands. There's no need to write function and returns. 7 (first function) and 5 lines (second function) have been reduced to 1 line:

```javascript
const multiplyByTwo = data.map(num => num * 2) // This does exactly the same as the previous function
```

### Take an array of numbers and convert them to strings






- Kenny