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
> The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

Javascript map() is a function that works the same as a traditional for loop but with benefits. So what's different?

### Multiplying by two
Let's say we want to loop over an array of numbers and multiply them by 2. Here's our array: 

```javascript
const data = [4, 8, 15, 16, 32, 42];
```

How would we multiply each number? A traditional for loop would look like this:

```javascript
function multiplyByTwo(arr) {
  // We create an empty array for future storage
  let newArr = []; 

  // Looping through the given array (const data), iterating through each item
  for (let i = 0; i < arr.length; i++) { 
    // Each iteration gets multiplied by two and pushed into the empty array
    newArr.push(arr[i] * 2); 
  }
  // Returning the array that now contains the new items pushed into it in the for loop
  return newArr; 
}
// Calling our function with the data array
console.log(multiplyByTwo(data)); 

// Returns an array of numbers multiplied by two
// [8, 16, 30, 32, 64, 84]
```

Using map, there's no need for a for loop as map does the looping for us. This shortens the code:

```javascript
function multiplyByTwo(arr) {
  return arr.map(function(num) { 
    return num * 2;
  })
}

console.log(multiplyByTwo(data));

// Returns an array of numbers multiplied by two
// [8, 16, 30, 32, 64, 84]
```

ES6 provides further shorthands. There's no need to write function and returns. 7 and 5 lines (first and second function respectively) have been reduced to 1 line:

```javascript
// This does exactly the same as the previous function
const multiplyByTwo = data.map(num => num * 2)
```

### Take an array of numbers and convert them to strings
Of course we can just as easily convert our numbers into strings using map.

```javascript
function convertToString(arr) {
  return arr.map(function(num) { 
    return num.toString();
  })
}

console.log(convertToString(data));

// Returns an array of strings
// ["4", "8", "15", "16", "32", "42"]
```

And with ES6:

```javascript
const convertToString = data.map(num => num.toString()) 

// Returns an array of strings
// ["4", "8", "15", "16", "32", "42"]
```




- Kenny