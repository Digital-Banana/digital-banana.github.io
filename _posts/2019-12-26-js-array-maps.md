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

Let's say we want to loop over an array of numbers and multiply them by 2. Here's our array: 

```javascript
const data = [4, 8, 15, 16, 32, 42];
```

How would we multiply each number? A traditional for loop would look like this:

```javascript
function multiplyByTwo(arr) {
  let newArr = [];
  for (let i = 0; i < arr.length; i++) {
    newArr.push(arr[i] * 2);
  }
  return newArr;
}

console.log(multiplyByTwo(data));
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

ES6 gives us further shorthands. There's no need to write function and returns:

```javascript
const multiplyByTwo = data.map(num => num * 2)
// This does exactly the same as the previous function
```

Thanks for reading!

- Kenny