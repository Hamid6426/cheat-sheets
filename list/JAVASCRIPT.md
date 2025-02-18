# JavaScript Cheat Sheet

## 📝 Basics
```js
// Single-line comment
/* Multi-line comment */

console.log("Hello, World!");   // Output to consol
let name = "Hamid";             // Variable (can be reassigned)
const PI = 3.14;                // Constant (cannot be reassigned)
var age = 25;                   // Older way
```
---
## DATA TYPES
```
let str = "Hello";   // String
let num = 42;        // Number
let bool = true;     // Boolean
let undef;           // Undefined
let empty = null;    // Null
let obj = { key: "value" }; // Object
let arr = [1, 2, 3]; // Array
```
## TYPE CHECK
```
console.log(typeof "Hello"); // "string"
console.log(typeof 42);      // "number"
console.log(typeof true);    // "boolean"
console.log(Array.isArray([])); // true
```
## ARITHMETIC OPERATORS
```
let add = a + b;   // Addition
let diff = c - d;  // Subtraction
let prod = a * b;  // Multiplication
let div = c / d;   // Division
x = 100 % 48;      // Modulo (Remainder)
let inc = a++;     // Postfix Increment
let dec = b--;     // Postfix Decrement
```
## BITWISE OPERATORS
```
a * (b + c)         // grouping
person.age          // member
person[age]         // member
!(a == b)           // logical not
a != b              // not equal
typeof a            // type (number, object, function...)
x << 2  x >> 3      // minary shifting
a = b               // assignment
a == b              // equals
a != b              // unequal
a === b             // strict equal
a !== b             // strict unequal
a < b   a > b       // less and greater than
a <= b  a >= b      // less or equal, greater or eq
a += b              // a = a + b (works with - * %...)
a && b              // logical and
a || b              // logical or
```
// Comparison
console.log(5 == "5");  // true (loose comparison)
console.log(5 === "5"); // false (strict comparison)
console.log(5 !== 3);   // true

// Logical
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true);         // false (NOT)

let x = 10;

// If-Else
if (x > 5) {
  console.log("Greater than 5");
} else if (x < 5) {
  console.log("Less than 5");
} else {
  console.log("Equal to 5");
}

// Switch
switch (x) {
  case 10:
    console.log("Ten");
    break;
  default:
    console.log("Not ten");
}

// For loop
for (let i = 0; i < 5; i++) {
  console.log(i);
}

// While loop
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}

// Do-While loop
let num = 0;
do {
  console.log(num);
  num++;
} while (num < 5);

// Function Declaration
function greet(name) {
  return "Hello, " + name;
}

// Function Expression
const greet = function(name) {
  return "Hello, " + name;
};

// Arrow Function
const greet = (name) => "Hello, " + name;

console.log(greet("Hamid")); // "Hello, Hamid"

let person = {
  name: "Hamid",
  age: 25,
  greet: function () {
    console.log("Hello, " + this.name);
  },
};

console.log(person.name); // "Hamid"
person.greet(); // "Hello, Hamid"

let fruits = ["Apple", "Banana", "Cherry"];

console.log(fruits[0]); // "Apple"

fruits.push("Mango"); // Add to end
fruits.pop();         // Remove from end
fruits.shift();       // Remove from start
fruits.unshift("Grapes"); // Add to start

console.log(fruits.length); // Length of array

let numbers = [1, 2, 3, 4, 5];

let doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]
let evens = numbers.filter(num => num % 2 === 0); // [2, 4]
let sum = numbers.reduce((acc, num) => acc + num, 0); // 15

console.log(doubled, evens, sum);

// Timeout
setTimeout(() => {
  console.log("Executed after 2 seconds");
}, 2000);

// Interval
let counter = 0;
let interval = setInterval(() => {
  console.log(counter++);
  if (counter > 3) clearInterval(interval);
}, 1000);

// Promises
let promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Data loaded"), 2000);
});

promise.then(data => console.log(data)).catch(err => console.log(err));

fetch("https://jsonplaceholder.typicode.com/posts")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error));

class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    return `Hello, my name is ${this.name}`;
  }
}

let user = new Person("Hamid", 25);
console.log(user.greet()); // "Hello, my name is Hamid"

// Template Literals
let name = "Hamid";
console.log(`Hello, ${name}`);

// Destructuring
let user = { name: "Hamid", age: 25 };
let { name, age } = user;

console.log(name, age); // "Hamid", 25

// Spread & Rest Operators
let arr1 = [1, 2, 3];
let arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

function sum(...nums) {
  return nums.reduce((a, b) => a + b);
}

console.log(sum(1, 2, 3, 4)); // 10

// Optional Chaining
let person = { profile: { name: "Hamid" } };
console.log(person?.profile?.name); // "Hamid"

// Exporting (export.js)
export const greeting = "Hello";
export function sayHello() {
  return "Hello World!";
}

// Importing (import.js)
import { greeting, sayHello } from "./export.js";

console.log(greeting); // "Hello"
console.log(sayHello()); // "Hello World!"
```
---

## Error Handling
```
try {
  let x = y; // y is undefined
} catch (error) {
  console.log("Error:", error.message);
} finally {
  console.log("This always runs");
}
```
