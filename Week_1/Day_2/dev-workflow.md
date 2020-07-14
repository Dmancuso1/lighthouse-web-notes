# DAY 2: The Dev Workflow - incremental development. 06/23/2020 

### Dominic Tremblay will be sending all the code from his lecture and also the zoom video..

## [link for the code](https://www.google.com) (if not there, check compass lecture notes)

### how to check if number has 1 digit?
* if number modulus 1 === 0 is true, then number has no decimal.

### Also checkout 'isNan(...)' in js
* if you want to check if something is NOT a number, then use this method.


### Refactoring
* it is nice to wrap bits of code in functions for readability as well as re-useability.

[Markup syntax!!!!](https://www.markdownguide.org/basic-syntax/)



# Coding Best Practices

### Rule 1
* Give your functions precise verb/action based names
### Rule 2
* Use camelCasedNames (like this one)
### Rule 3
* Properly indent the function code
### Rule 4
* Functions should focus on a single task: returning a value or causing a side effect. Break your function into additional smaller functions if you find it doing two or more things
  * One single task could be to compute and return a value (eg: zeroPad)
  * Another single task could be to perform a side effect such as logging a message to the screen (eg: printFarmInventory)
### Rule 5:
* It is ideal if functions try to avoid reading outer scope variables. If a function needs some information / data, then that data should instead be passed in as a parameter, making it available within the function's inner scope.
* Data needed by Functions should be passed in as parameters/arguments (i.e. local scope) instead of being accessed directly

# Some Notes on Truthy/falsey

```
// All of the following are inherently falsey:

False
// False is False. Makes sense, right?

0
// 0 is the only falsey Number

""
// an empty string is falsey

null
// a null, or empty value, is falsey.

undefined
// an object that has not been defined is considered falsey.

NaN
// Not a Number. You'll learn more about NaN as we go on.
```

<br/>

## This is a simple way to check if our list is empty:

```
shoppingList = [];

if (!shoppingList.length) {
  shoppingList.push('coconut milk');
}
```

