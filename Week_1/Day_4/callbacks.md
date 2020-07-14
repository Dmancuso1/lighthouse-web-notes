# Functions

Functions are first-class objects.

This means two important things:

* Functions can be stored in variables and passed around
* Functions can do everything that other objects can do (like having properties assigned to them)

## Callbacks

The most notable usage of having functions as values in JavaScript is a <b>callback function</b>.

* Is a function passed (by reference) into another function (let's call that one the "receiver" function)
* The receiver function is therefore accepting behavior to perform by calling the callback function that it now has access to
* The receiver function can decide to call the callback function at any time, as many times as it wants

```
// The second argument/parameter is expected to be a (callback) function
const findWaldo = function(names, found) {
  for (let i = 0; i < names.length; i++) {
    let name = names[i];
    if (name === "Waldo") {
      found();   // execute callback
    }
  }
}

const actionWhenFound = function() {
  console.log("Found him!");
}

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```



This code illustrates how a function can be treated as an ordinary value and passed around to another function. We pass a reference to the function named actionWhenFound as an argument to another function findWaldo.

The function actionWhenFound is known as a callback function. It is first defined, then passed as an argument to another function, and finally executed once a specific event occurs.


## Arrow functions
```
// BEFORE: anonymous callback as function expression 
[1,2,3].forEach(function (num) {
  console.log('num: ', num);
});

// AFTER: anonymous callback as arrow function
[1,2,3].forEach((num) => {
  console.log('num: ', num);
});
```

<br/>

## Higher ORder Functions

* Spoiler Alert: Functions that take in callbacks are referred to as Higher Order Functions.
* Higher-Order functions are any functions which operate on other functions.
* This includes, but is not limited to, functions which take in functions (callbacks) as arguments.
* This means that built-in functions such as forEach, filter, and others can be called "Higher-Order Functions".