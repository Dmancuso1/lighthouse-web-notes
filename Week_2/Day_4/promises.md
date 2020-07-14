# Promises


## Review of Callbacks

Anytime we pass a function X into another function Y to be called by that function Y, X can be referred to as a callback function.

helps with asynch workflow because javascript is 'single threaded'.

asyn functions cannot RETURN. to avoid this, we can use a callbacks (eventually use promises)
 to get the data)

(opposite is a higher order function.. which calls another function within it) (parent function)

## What are promises?

Promises are objects with certain behaviours.
  -  They always start out pending.
  - we must explicitly use functions that support.use promises
  - Promises have a `.then` method for us to attach/provide callback as a seperate step.
  - The .then method on a promise also returns a (new) promise. 
  - The final result of the .then callback is what the new promise evaluates to.  We keep passing data through to the next .then.. by the end you have all your data (assuming you're trying to load files in order or something).
