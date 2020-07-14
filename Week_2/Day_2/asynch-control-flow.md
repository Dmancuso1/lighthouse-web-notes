# Asynchronous Control Flow

* ## Review Callbacks
  * higher order functions takes a function (callback) as a param..
  * what is the purpose ? the same way one func makes code reusable.. having a function using a function inside makes it even more modular. 
  * Callbacks are used really often in asynch applicaitons.
* ## Synchronous comtrol flow
  * single thread JS

* ## Asynch control flow
  * Asynchronous runs after Synchronous code
* ## Asynch actions
* ## Set Time out
  * `setTimeOut` (runs a callback at a later time once )
   * `setInterval` interval, runs a callback at a specific interval (or whatever delay you set for it).
      * Stop setInterval from running with an 'interval id' which can be stored in a variable `returnId` <- this is an object. 
* ## File system functions
  * use "fs" to access files in node. ie" `const fs = require('fs')` <- node/JS knows what this is.
* ## Events and event handlers
  * Handeling User Input
    * in node we can do: `process.stdin` and `process.stdout`- which allows us to listen to input and run a callback during that input. 