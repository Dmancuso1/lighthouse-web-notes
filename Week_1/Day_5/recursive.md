# Recursion

Recursion is basically a function that keeps running until it doesn't.
if can be used to do the same thing loops do.
see doe below. Function will run until it's parameter meets a certain condition.

```
function countEvenToTwelve(number) {
  if (number <= 12) {
    console.log(number);
    countEvenToTwelve(number+2);
}
countEvenToTwelve(0);
```
<br>

## Special note:
Every recursive function must stop calling itself at some point, otherwise it will just continue to call itself forever, like an infinite loop. The following function never stops calling itself.

<br>

## Also..
The recursive case is when the function will continue to call itself. Every time the function calls itself, the input gets closer and closer to the base case. The base case is when the function no longer calls itself. In a properly designed recursive function, with each recursive call, the input must gradually resolve toward the base case.

A function must have at least one recursive case and at least one base case in order to be recursive.

<br>

## Conclusion 
Recursion is a tool you can use as an alternative to traditional iteration using for and while loops.

Every recursive function must have a base case and a recursive case.
Each recursive call should break down the current problem into a smaller, simpler one.
The recursive calls must eventually reach the smallest version of the problem, the base case.
The base case is when the problem can be solved without further recursion.