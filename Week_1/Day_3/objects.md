# Objects in JS

<p>Objects are a way to store data, BUT instead of having an INDEX and a val, it has a KEY and a VALUE.


in Objects, the order of things and how you store them does not matter

how to we add to an ojbect?
In Objects there are two ways of storing a key/value pair.
* 1st way: obj.color = 'red' .. the only way we can store is because we define a key name ourselves.
* When you have a variable with a value inside of a variable that YOU WANT TO BE THE KEY, we must use the square bracket notation.
declare variableName..
example: obj[variableName] = 'the value'</p>

You can use a FOR..IN loop  (also experiment with For..of loop)
``` 
for (let i in obj) {
  console.log(i) // is the KEY!! :)
  console.log(obj[i]) // these are the Values! :)
}
```
<br>

## Example: 

``` 
const obj = {
  fName: "Dane",
  lName: "Mancuso",
  gender: "Male"
}

let address = "address";
obj[address] = "123 milky way, Universe, 42";

for (let i in obj) {
  console.log(i + " = " + obj[i]);
}
```
## Output:
```
fName = Dane
lName = Mancuso
gender = Male
address = 123 milky way, Universe, 42
```
<br>

## Another Example:

```
let obj = {
  a: 99, 
  b:1
}
const swap = function(object) {
  // how can acess values inside of object?
  console.log(object.b);
  // how to take value from object and assign to a variable.
  let tempValB = object.b;
  let tempValA = object.a
  // console.log('temp Val ====>', tempVal)
  // how can i assign a value to an object?
  object.a = tempValB;
  object.b = tempValA;
}
console.log('Object before', obj)
swap(obj);
console.log('Object After', obj);
```
## Output:
```
Object before { a: 99, b: 1 }
1
Object After { a: 1, b: 99 }
```

<br>

## More Cool info on Objects

* To inspect an object's keys, there is a method Object.keys(ObjName) that returns an array of keys.

* Object.values(myObject), returns values.
* Object.keys(myObject), returns values.

<br>

## Let's review the six types of primitives:
* undefined
* null
* boolean
* string
* number
* symbol (Introduced in ES6 and not something we need to focus on right now)

<br>

## More on objects.

#### In later version of JS, you can assign one or multiple variables to the same object with below syntax.
```
const {name, icon, price} = item
// const name = item.name
// const icon = item.icon
// const price = item.price
```

## Also ! Check this Cool Syntax out.

#### Property value Shorthands

Property value shorthands let you abbreviate the definition of a property in an object literal: If the name of the variable that specifies the property value is also the property key then you can omit the key. This looks as follows:

```
const x = 4;
const y = 1;
const obj = { x, y };
```
The Last Line is equivalent to:
```
const obj = { x: x, y: y };
```


Property value shorthands work well together with destructuring:
```
const obj = { x: 4, y: 1 };
const {x,y} = obj;
console.log(x); // 4
console.log(y); // 1
```
<br>

#### Another exmaple how to use this syntax:

```
let cat = 'Miaow';
let dog = 'Woof';
let bird = 'Peet peet';

let someObject = {
  cat,
  dog,
  bird
}

console.log(someObject);

//{
//  cat: "Miaow",
//  dog: "Woof",
//  bird: "Peet peet"
//}
```

### The longer/older way:
```
var cat = 'Miaow';
var dog = 'Woof';
var bird = 'Peet peet';

var someObject = {
  cat: cat,
  dog: dog,
  bird: bird
}
```