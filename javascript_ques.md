## Core JavaScript Concepts

#### Q1. What is JavaScript?

JavaScript is a high-level, interpreted programming language commonly used for creating dynamic and interactive web pages. It enables adding functionality and behavior to websites.

#### Q2. Data Types

- Primitive and Reference Data Types
- JavaScript has two main data types:

  - `Primitive data types`: These are simple data types that hold single values. Examples include number, string, boolean, null, undefined, and symbol.
  - `Reference data types:` These data types (objects) hold collections of other data and are passed by reference. Changes made to a reference data type are reflected in the original object.

    ```js
    console.log(typeof 10); // Output: "number" (primitive)
    console.log(typeof "Hello"); // Output: "string" (primitive)
    console.log(typeof true); // Output: "boolean" (primitive)
    const person = { name: "Alice", age: 30 };
    console.log(typeof person); // Output: "object" (reference)
    ```

#### Q3. Variables & Scope

var, let, and const
JavaScript provides three ways to declare variables:

- `var`: This has function-scoped or global scope (depending on placement) and can be re-declared and re-assigned. Use it with caution due to potential scoping issues.
- `let`: This has block-level scope and can be re-assigned but not re-declared within the same block. It's generally preferred for modern JavaScript due to its better scoping.
- `const`: This creates a constant variable that cannot be re-assigned after its initial declaration. Use it for values that shouldn't change.

  ```js
  if (true) {
    var x = 10;
    let y = 20;
    const z = 30;
  }
  console.log(x); // Accessible outside the block (var)
  console.log(y); // ReferenceError: y is not defined (let)
  console.log(z); // ReferenceError: z is not defined (const)
  ```

#### Q4. Operators

- `Arithmetic operators`: +, -, \*, /, % (modulo)
- `Comparison operators:` ==, !=, ===, !==, <, >, <=, >=
- `Logical operators`: && (AND), || (OR), ! (NOT)
- `Assignment operators`: =, +=, -=, \*=, /=, %=
- `Other operators:` typeof, delete, in, instanceof

#### Q5. Control Flow

- if statements: Execute code conditionally based on a boolean expression.
- else if statements: Provide additional conditions to check after an if statement.
- else statements: Execute code if none of the preceding conditions are true.
- switch statements: Execute code based on a matched case value.
- Loops:
  - for loops: Execute code repeatedly based on a counter and conditions.
  - while loops: Execute code repeatedly as long as a condition is true.
  - do-while loops: Execute code at least once, then repeatedly as long as a condition is true.

#### Q6. Functions

- Function declaration and expression syntax.
- Parameters and arguments.
- Return values.
- Function scope.
- Closures (explained later in Advanced Concepts).

  ```js
  function sum(a, b) {
    return a + b;
  }
  const result = sum(5, 10);
  console.log(result); // Output: 15
  ```

### Q7. Arrays

- Array creation using literals ([]) and constructor (new Array()).
- Accessing elements using index notation (array[index]).
- Modifying elements using assignment (array[index] = value).
- Common methods: push, pop, shift, unshift, slice, splice, concat, indexOf, lastIndexOf, join, and more.
  ```js
  const numbers = [1, 2, 3, 4];
  console.log(numbers[1]); // Output: 2
  numbers.push(5);
  console.log(numbers); // Output: [1, 2, 3, 4]
  ```

#### Q8. Objects

- Object literals ({}) and constructor (new Object()).
- Key-value pairs for storing data.
- Accessing properties using dot notation (object.property) and bracket notation (object["property"]).
- Defining methods (functions within objects).

  ```js
  const person = {
    name: "Alice",
    age: 30,
    greet() {
      console.log("Hello, my name is " + this.name);
    },
  };
  person.greet(); // Output: Hello, my name is Alice
  ```

#### Q9. Prototypes & Inheritance

- Prototype-based inheritance in JavaScript.
- The prototype property of objects.
- Creating new objects inheriting properties from a prototype.
- Note: This is a more advanced concept, so explanations and code examples can be tailored for intermediate candidates.

#### Q10. ES6+ Features

- Arrow functions (const sum = (a, b) => a + b;)
- Destructuring (const [x, y] = [1, 2];)
- Spread syntax (const numbers = [...arr1, ...arr2];)
- Template literals (const message =Hello, ${name}!;)
- Classes (class Person { ... })
- Modules (import, export)

#### Q11. Closures

#### Q12. Asynchronous Programming

- Callbacks (function(data) { ... }))
- Promises (new Promise((resolve, reject) => { ... }))
- Async/await (async function - fetchData() { ... })
- Explain the differences and use cases for these techniques in handling asynchronous operations.

#### Q13. Error Handling

- try...catch blocks for handling exceptions.
- throw statements for throwing custom errors.
  ```js
  try {
    const result = x / 0; // Assuming x is 0
    console.log(result);
  } catch (error) {
    console.error("Error:", error.message);
  }
  ```

#### Q14. DOM Manipulation

- Explain how JavaScript interacts with the Document Object Model (DOM).
- Common methods for accessing and modifying HTML elements (e.g., getElementById, createElement, setAttribute).
- `Note`: Basic understanding of DOM manipulation is helpful for most JavaScript developer roles.

#### Q15. Event Handling

- Attaching event listeners (element.addEventListener("click", function() { ... }))
- Handling user interactions (clicks, key presses, etc.)
  ```js
  const button = document.getElementById("myButton");
  button.addEventListener("click", function () {
    alert("Button clicked!");
  });
  ```

#### Q16. Currying

Currying is a technique for transforming a function that takes multiple arguments into a sequence of functions, each of which takes a single argument. It's helpful for creating reusable functions with partial application.

```js
function add(a) {
  return function (b) {
    return a + b;
  };
}
const add5 = add(5); // Curried function to add 5 to a number
console.log(add5(10)); // Output: 15
```

Explanation:

- The add function takes one argument (a) and returns another function.
- The inner function takes another argument (b) and returns the sum of a and b.
- When we call add(5), the inner function is returned, pre-filling a with 5.
- Calling add5(10) then adds 10 to the pre-filled a (which is 5).

#### Q17. Closures

Closures are a way to create private variables within functions. A closure is a function that has access to the variable environment (including variables) of the outer function in which it was created, even after the outer function has returned.

```js
function createCounter() {
  let count = 0; // Private variable (not directly accessible from outside)
  return function () {
    count++;
    return count;
  };
}
const counter1 = createCounter();
const counter2 = createCounter();
console.log(counter1()); // Output: 1 (initial count)
console.log(counter1()); // Output: 2
console.log(counter2()); // Output: 1 (separate counter)
```

Explanation:

- The createCounter function defines a private variable count.
- It returns an inner function that has access to count even after createCounter has finished executing.
- Calling createCounter multiple times creates closures with separate instances of count, making them independent counters.

#### Q18. Promises

Promises are an object representing the eventual completion (or failure) of an asynchronous operation. They provide a way to handle asynchronous code in a more structured and readable manner.

```js
function fetchData(url) {
  return new Promise((resolve, reject) => {
    const xhr = new XMLHttpRequest();
    xhr.open("GET", url);
    xhr.onload = function () {
      if (xhr.status === 200) {
        resolve(JSON.parse(xhr.responseText));
      } else {
        reject(new Error("Failed to fetch data"));
      }
    };
    xhr.send();
  });
}

fetchData("https://api.example.com/data")
  .then((data) => console.log(data)) // Handle successful response
  .catch((error) => console.error(error.message)); // Handle errors
```

Explanation:

- The fetchData function takes a URL and returns a Promise.
- Inside the Promise, an XHR request is made to fetch data.
- The onload callback handles the response:
  - If successful (status 200), the Promise is resolved with the parsed JSON data.
  - If there's an error, the Promise is rejected with an error object.
- We use then and catch to handle the resolved data and potential errors, respectively.

#### Q19. Async/Await

Async/await syntax is built on top of Promises and provides a more synchronous-like way to write asynchronous code. It makes handling asynchronous operations easier to read and manage.

```js
async function fetchDataAsync(url) {
  try {
    const response = await fetch(url);
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error.message);
  }
}

fetchDataAsync("https://api.example.com/data");
```

Explanation:

- The fetchDataAsync function is declared as async.
- The await keyword is used before asynchronous operations like fetch and json().
- The function pauses execution at each await until the promise resolves, then continues with the next step.
- Error handling is done within a try...catch block.

#### Q20. Higher-Order Functions (HOFs)

HOFs are functions that take other functions as arguments or return functions as results. They enable powerful abstractions and code reusability.

Questions:

- Explain what Higher-Order Functions (HOFs) are and provide examples.
- How can HOFs be used to improve code reusability and maintainability?
- Discuss common HOFs like map, filter, reduce, and forEach. When would you use each?

```js
const numbers = [1, 2, 3, 4];

const doubledNumbers = numbers.map((number) => number * 2); // [2, 4, 6, 8]

const evenNumbers = numbers.filter((number) => number % 2 === 0); // [2, 4]

const total = numbers.reduce((acc, number) => acc + number, 0); // 10
```

#### Q21. The Spread Operator (...)

The spread operator (...) allows you to efficiently expand iterables like arrays and objects into individual elements or property values.

Questions:

- Explain the functionality of the spread operator (...) in JavaScript.
- How can the spread operator be used for copying arrays and objects?
- Provide examples of using the spread operator to combine arrays or object literals.

```js
const numbers1 = [1, 2, 3];
const numbers2 = [4, 5, 6];

const combinedNumbers = [...numbers1, ...numbers2]; // [1, 2, 3, 4, 5, 6]

const person1 = { name: "Alice" };
const person2 = { age: 30 };

const combinedPerson = { ...person1, ...person2 }; // { name: "Alice", age: 30 }
```

#### Q22. Destructuring

Destructuring is a syntactic sugar for extracting values from arrays or properties from objects into distinct variables.

Questions:

- What is destructuring in JavaScript? Explain array destructuring and object destructuring.
- How can destructuring be used to make code more concise and readable?
- Provide examples of destructuring default values and the rest operator (...).

```js
const numbers = [10, 20, 30];

const [first, second] = numbers; // first = 10, second = 20

const person = { name: "Bob", age: 25 };

const { name } = person; // name = "Bob"

const [name, age = 18] = ["Charlie"]; // name = "Charlie", age = 18 (default value)
```

#### Q23. Arrays

- Array methods: Deep dive into methods like map, filter, reduce, forEach, some, every, find, findIndex, sort, and more. Understand their use cases and how they can improve code conciseness and readability.
- Array destructuring: Utilize array destructuring to extract specific elements from arrays into separate variables. This can make code more readable and concise.
- Spread operator (...) with arrays: Learn how to use the spread operator to combine arrays, create copies, and pass elements as arguments to functions.
- Iterators and generators with arrays: Understand how to create custom iterators for arrays and explore generators for creating iterators lazily.

#### Q24. Functional Programming (FP)

Functional programming (FP) emphasizes treating functions as first-class citizens and focuses on immutability. Here are some key areas to understand:

- Pure functions: Functions that always return the same output for the same input and have no side effects (don't modify external state).
- Immutability: Creating new data structures instead of modifying existing ones.
- Higher-order functions (HOFs): Functions that take other functions as arguments or return functions as results. Common HOFs include map, filter, reduce, and forEach.

#### Q25. DOM Manipulation

While basic DOM manipulation is essential, focus on deeper understanding:

- Event handling: Understand how to attach event listeners to DOM elements and handle user interactions (clicks, key presses, etc.).
- DOM traversal: Explore methods like querySelector, querySelectorAll, getElementById, and getElementsByTagName for efficiently navigating the DOM tree.
- DOM manipulation techniques: Learn how to create, modify, and remove elements from the DOM using methods like createElement, setAttribute, appendChild, and removeChild.
- Virtual DOM (optional): If applicable to the role, understand the concept of virtual DOM used by libraries like React and its advantages.
