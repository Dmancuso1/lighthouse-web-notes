# Weekend ! - Modules and testing


## Modules

Every Node file is a module and we can check this by running 
```
console.log(module)
```
<b>This is What we get 😄</b>
```
Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/vagrant/w1/d6-testing/moduleCheck.js',
  loaded: false,
  children: [],
  paths:
   [ '/vagrant/w1/d6-testing/node_modules',
     '/vagrant/w1/node_modules',
     '/vagrant/node_modules',
     '/node_modules' ] }
     ```Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/vagrant/w1/d6-testing/moduleCheck.js',
  loaded: false,
  children: [],
  paths:
   [ '/vagrant/w1/d6-testing/node_modules',
     '/vagrant/w1/node_modules',
     '/vagrant/node_modules',
     '/node_modules' ] }
```
<br>

## Require and Export

### Require:

```
const sayHelloTo = require('./myModule');
// or 
const sayHelloTo = require("./myModule.js");
```

### Export 

```
// add this line to the end of the file.
module.exports = sayHelloTo;

```
<br>

### We learned that in Node,

* modules are its way of organizing code into individual files
* every js file in node is implicitly a module
  * we can console.log(module) and see its details
* module.exports tells node what to export from a file
  * it defaults to {}
* we can use require with relative paths (like ./myModule)
* it doesn't need the .js extension, as that is implied

# More testing.. 
## Unit Testing

Unit testing is the practice of testing small pcs of code, typically individual functions, alone and isolated. Mocha is a popular tool
[See more from codeutopia.net](https://codeutopia.net/blog/2015/04/11/what-are-unit-testing-integration-testing-and-functional-testing/)

## Integration Testing.
As the name suggests, in integration testing the idea is to test how parts of the system work together – the integration of the parts. Integration tests are similar to unit tests, but there’s one big difference: while unit tests are isolated from other components, integration tests are not. For example, a unit test for database access code would not talk to a real database, but an integration test would.
[See more from codeutopia.net](https://codeutopia.net/blog/2015/04/11/what-are-unit-testing-integration-testing-and-functional-testing/)

## Functional Testing
Functional testing is also sometimes called E2E testing, or browser testing. They all refer to the same thing.

Functional testing is defined as the testing of complete functionality of some application. In practice with web apps, this means using some tool to automate a browser, which is then used to click around on the pages to test the application.
[See more from codeutopia.net](https://codeutopia.net/blog/2015/04/11/what-are-unit-testing-integration-testing-and-functional-testing/)

### Note:
Unit tests should be your main focus when testing JavaScript code. They are the easiest to write and maintain, and provide many benefits beyond reducing bugs. Integration and functional tests should be in a supporting role, for where unit tests are not suitable.

### More on Unit Testing..

Unit testing, when done correctly, is a magic button that tells us if our code is working. But instead of a button, it's a terminal command. And instead of magic, it's just ``` npm test. ```


# Mocha And Chai for Unit Testing.

With Node installed, open up a terminal or command line in your project’s directory.

If you want to test code in the browser, run ``` npm install mocha chai --save-dev ```
If you want to test Node.js code, in addition to the above, run ```npm install -g mocha```

<br>
This installs the packages mocha and chai. Mocha is the library that allows us to run tests, and Chai contains some helpful functions that we’ll use to verify our test results.

## Directory Structure:

You should put your tests in a separate directory from your main code files. This makes it easier to structure them, for example if you want to add other types of tests in the future (such as integration tests or functional tests).

The most popular practice with JavaScript code is to have a directory called test/ in your project’s root directory. Then, each test file is placed under test/someModuleTest.js. Optionally, you can also use directories inside test/, but I recommend keeping things simple — you can always change it later if necessary.