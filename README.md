# JavaScript Interview Questions and Answers 🚀

Welcome to the **JavaScript Interview Preparation Repository**!  
This repo is designed to help **you or anyone preparing for front-end or full-stack roles** get a strong grip on JavaScript, from fundamentals to advanced concepts.

Whether you're a beginner brushing up on core topics or an experienced developer preparing for senior-level interviews, this guide covers **all the essential questions**, broken down with **detailed explanations**, **examples**, and **interview-ready answers**.

We’ve categorized the questions into:

- ✅ **Beginner** – Core language fundamentals
- ⚡ **Intermediate** – Concepts used in day-to-day development
- 🔥 **Advanced** – Deep-dive into internals and performance topics

Use the **Table of Contents** below to navigate quickly. Each answer includes a `[🔝 Back to Top](#table-of-contents)` link for easy access.

---

## Table of Contents

### 🟢 Beginner Level (Fundamentals)

1. [What is JavaScript and how is it different from Java?](#1-what-is-javascript-and-how-is-it-different-from-java)
2. [Explain var, let, and const with examples.](#2-explain-var-let-and-const-with-examples)
3. [What are data types in JavaScript?](#3-what-are-data-types-in-javascript)
4. [What are truthy and falsy values?](#4-what-are-truthy-and-falsy-values)
5. [Explain double(==) vs triple(===).](#5-explain-double-vs-triple)
6. [What is hoisting in JavaScript?](#6-what-is-hoisting-in-javascript)
7. [What is the difference between null and undefined?](#7-what-is-the-difference-between-null-and-undefined)
8. [What is scope in JavaScript?](#8-what-is-scope-in-javascript)
9. [What are closures in JavaScript?](#9-what-are-closures-in-javascript)
10. [What is the difference between function declaration and function expression?](#10-what-is-the-difference-between-function-declaration-and-function-expression)

### 🟡 Intermediate Level

11. [What is the event loop in JavaScript?](#11-what-is-the-event-loop-in-javascript)
12. [Explain call, apply, and bind methods in javascript.](#12-explain-call-apply-and-bind-methods-in-javascript)
13. [What are arrow functions and how are they different?](#13-what-are-arrow-functions-and-how-are-they-different)
14. [What is the difference between synchronous and asynchronous code?](#14-what-is-the-difference-between-synchronous-and-asynchronous-code)
15. [What is a promise and how does it work?](#15-what-is-a-promise-and-how-does-it-work)
16. [What is async/await and how does it work under the hood?](#16-what-is-asyncawait-and-how-does-it-work-under-the-hood)
17. [What is the difference between map, filter, and reduce?](#17-what-is-the-difference-between-map-filter-and-reduce)
18. [What are template literals?](#18-what-are-template-literals)
19. [What are higher-order functions?](#19-what-are-higher-order-functions)
20. [What is the difference between shallow and deep copy?](#20-what-is-the-difference-between-shallow-and-deep-copy)

### 🔵 Advanced Level

21. [What is prototypal inheritance?](#21-what-is-prototypal-inheritance)
22. [What is the difference between Object.create() and class?](#22-what-is-the-difference-between-objectcreate-and-class)
23. [Explain currying in JavaScript.](#23-explain-currying-in-javascript)
24. [What is debouncing and throttling?](#24-what-is-debouncing-and-throttling)
25. [What is memory leak in JavaScript and how to avoid it?](#25-what-is-memory-leak-in-javascript-and-how-to-avoid-it)
26. [What is the difference between setTimeout and setInterval?](#26-what-is-the-difference-between-settimeout-and-setinterval)
27. [What is event delegation?](#27-what-is-event-delegation)
28. [How does JavaScript garbage collection work?](#28-how-does-javascript-garbage-collection-work)
29. [What are Web APIs in the browser?](#29-what-are-web-apis-in-the-browser)
30. [How do modules work in JavaScript (CommonJS vs ES Modules)?](#30-how-do-modules-work-in-javascript-commonjs-vs-es-modules)

---

### 1. What is JavaScript and how is it different from Java?

**JavaScript** is a lightweight, interpreted, high-level programming language that is primarily used to build dynamic and interactive web pages. It is a **core technology of the web**, alongside HTML and CSS.

Despite the similar names, **JavaScript and Java are completely different languages** in terms of design, syntax, and use cases.

#### ✅ Key Characteristics of JavaScript:

- **Interpreted** (not compiled)
- **Dynamically typed**
- **Prototype-based inheritance**
- Runs in the browser and also on the server (Node.js)
- Supports **event-driven**, **asynchronous**, and **functional** programming

#### ✅ Differences Between JavaScript and Java:

| Feature         | JavaScript                                   | Java                                       |
| --------------- | -------------------------------------------- | ------------------------------------------ |
| **Type**        | Scripting Language                           | Object-Oriented Programming Language       |
| **Execution**   | Interpreted                                  | Compiled (into bytecode, then run on JVM)  |
| **Environment** | Browser, Node.js                             | JVM (Java Virtual Machine)                 |
| **Typing**      | Dynamically typed                            | Statically typed                           |
| **Syntax**      | Loosely written (no class needed)            | Strict class-based syntax                  |
| **Concurrency** | Event-driven, non-blocking (single-threaded) | Multi-threaded via threads                 |
| **Use Case**    | Web interactivity, frontend/backend logic    | Enterprise apps, Android, desktop, backend |

#### 📌 Example:

**JavaScript**

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet("Atikur")); // Hello, Atikur!
```

**Java**

```java
public class Main {
  public static void main(String[] args) {
    System.out.println(greet("Atikur"));
  }

  static String greet(String name) {
    return "Hello, " + name + "!";
  }
}
```

#### 🧠 Summary:

- JavaScript is used primarily for **web development**, while Java is used for **enterprise, Android, and backend** applications.
- JavaScript is **loosely typed and dynamic**, whereas Java is **strongly typed and static**.
- They **do not share any runtime, libraries, or design philosophy** despite having similar names.

---

[🔝 Back to Top](#table-of-contents)

### 2. Explain var, let, and const with examples

In JavaScript, `var`, `let`, and `const` are used to declare variables, but they differ in **scope**, **hoisting behavior**, and **reassignment rules**.

---

#### 1️⃣ **var**

- **Scope**: Function-scoped (available throughout the function where it’s declared).
- **Hoisting**: Hoisted to the top of its scope and initialized with `undefined`.
- **Redeclaration**: Allowed in the same scope.
- **Reassignment**: Allowed.

```javascript
function testVar() {
  console.log(a); // undefined (due to hoisting)
  var a = 10;
  console.log(a); // 10
}
testVar();

// Redeclaration allowed
var x = 5;
var x = 20;
console.log(x); // 20
```

---

#### 2️⃣ **let**

- **Scope**: Block-scoped (only available inside `{}` where it's declared).
- **Hoisting**: Hoisted but **not initialized** (in the _Temporal Dead Zone_ until assigned).
- **Redeclaration**: **Not allowed** in the same scope.
- **Reassignment**: Allowed.

```javascript
function testLet() {
  // console.log(b); // ❌ ReferenceError (Temporal Dead Zone)
  let b = 10;
  console.log(b); // 10
}
testLet();

// Redeclaration not allowed
let y = 5;
// let y = 20; // ❌ SyntaxError
y = 15; // ✅ Allowed
console.log(y); // 15
```

---

#### 3️⃣ **const**

- **Scope**: Block-scoped.
- **Hoisting**: Hoisted but not initialized (Temporal Dead Zone).
- **Redeclaration**: Not allowed in the same scope.
- **Reassignment**: Not allowed (the variable binding is constant, but object/array contents can be mutated).

```javascript
const z = 10;
// z = 20; // ❌ TypeError (can't reassign)

// With objects
const person = { name: "Atikur" };
person.name = "Satter"; // ✅ Allowed (object reference unchanged)
console.log(person); // { name: "Satter" }
```

---

#### 📊 **Comparison Table**

| Feature           | var                              | let                      | const                    |
| ----------------- | -------------------------------- | ------------------------ | ------------------------ |
| **Scope**         | Function-scoped                  | Block-scoped             | Block-scoped             |
| **Hoisting**      | Yes (initialized as `undefined`) | Yes (TDZ until assigned) | Yes (TDZ until assigned) |
| **Redeclaration** | ✅ Allowed                       | ❌ Not allowed           | ❌ Not allowed           |
| **Reassignment**  | ✅ Allowed                       | ✅ Allowed               | ❌ Not allowed           |

---

#### 🧠 Key Takeaways:

- Prefer **`let`** and **`const`** in modern JavaScript.
- Use **`const`** by default unless you know the variable will change.
- Avoid `var` in modern code to prevent scope-related bugs.

---

[🔝 Back to Top](#table-of-contents)

### 3. What are data types in JavaScript?

JavaScript variables can hold different types of data.  
Data types define the **kind of values** that can be stored and how they behave in operations.

---

## 📌 Two Main Categories of Data Types

### 1️⃣ **Primitive Data Types** (Immutable, stored by value)

Primitive types are simple, immutable values.  
When assigned to a variable, they are **copied** rather than referenced.

1. **String**
   ```javascript
   let name = "Atikur";
   let greeting = "Hello";
   let template = `Hi, ${name}`;
   ```

````

2. **Number**

   ```javascript
   let age = 25;
   let price = 99.99;
   let infinityValue = Infinity;
   let notANumber = NaN;
   ```

3. **Boolean**

   ```javascript
   let isActive = true;
   let isComplete = false;
   ```

4. **Undefined**

   ```javascript
   let a;
   console.log(a); // undefined
   ```

5. **Null**

   ```javascript
   let b = null;
   console.log(b); // null
   ```

6. **Symbol** (ES6)

   ```javascript
   let id = Symbol("uniqueId");
   let id2 = Symbol("uniqueId");
   console.log(id === id2); // false
   ```

7. **BigInt** (ES2020)

   ```javascript
   let bigNumber = 123456789012345678901234567890n;
   ```

---

### 2️⃣ **Non-Primitive (Reference) Data Types**

These are objects, arrays, and functions.
They are stored **by reference**, meaning multiple variables can point to the same object in memory.

1. **Object**

   ```javascript
   let person = { name: "Atikur", age: 25 };
   ```

2. **Array**

   ```javascript
   let colors = ["red", "green", "blue"];
   ```

3. **Function**

   ```javascript
   function greet() {
     return "Hello!";
   }
   ```

---

### 🧠 Key Notes:

* **typeof null** returns `"object"` (a historical JavaScript bug).
* **Arrays** and **functions** are technically objects.
* Primitive values are copied, but objects are referenced.

---

### 📊 Type Detection

```javascript
console.log(typeof "Hello"); // string
console.log(typeof 42);      // number
console.log(typeof true);    // boolean
console.log(typeof undefined); // undefined
console.log(typeof null);    // object (quirk)
console.log(typeof Symbol("id")); // symbol
console.log(typeof 123n);    // bigint
console.log(typeof {});      // object
console.log(typeof []);      // object
console.log(typeof function(){}); // function
````

---

[🔝 Back to Top](#table-of-contents)

### 4. What are truthy and falsy values?

In JavaScript, every value is inherently either **truthy** or **falsy** when evaluated in a **Boolean context** (e.g., in `if` conditions).

---

## 1️⃣ **Falsy Values**

These are values that evaluate to `false` when converted to a Boolean.

There are **only 6 falsy values** in JavaScript:

1. `false`
2. `0` (zero)
3. `""` (empty string)
4. `null`
5. `undefined`
6. `NaN`

📌 Example:

```javascript
if (false) console.log("Won't run");
if (0) console.log("Won't run");
if ("") console.log("Won't run");
if (null) console.log("Won't run");
if (undefined) console.log("Won't run");
if (NaN) console.log("Won't run");
```

---

## 2️⃣ **Truthy Values**

All values **other than falsy** are considered truthy.

Examples of truthy values:

- Non-empty strings: `"Hello"`, `" "`
- Non-zero numbers: `1`, `-5`, `3.14`
- Objects: `{}`, `[]`
- Functions: `function() {}`
- `Infinity` and `-Infinity`

📌 Example:

```javascript
if ("Hello") console.log("Runs - non-empty string is truthy");
if (42) console.log("Runs - non-zero number is truthy");
if ([]) console.log("Runs - empty array is truthy");
if ({}) console.log("Runs - empty object is truthy");
```

---

## 3️⃣ Boolean Conversion

You can explicitly check truthy/falsy nature using `Boolean()` or `!!`:

```javascript
console.log(Boolean("Hello")); // true
console.log(Boolean("")); // false
console.log(!!42); // true
console.log(!!0); // false
```

---

## 🧠 Key Takeaways:

- JavaScript automatically converts values to Boolean when needed (type coercion).
- Knowing falsy values helps avoid **unexpected bugs** in conditions.
- Always use strict comparisons (`===`) if you need to differentiate between values like `0`, `null`, or `undefined`.

[🔝 Back to Top](#table-of-contents)

### 5. Explain double(==) vs triple(===)

In JavaScript, both `==` and `===` are comparison operators, but they behave differently when comparing values.

---

## 1️⃣ **`==` (Loose Equality / Abstract Equality)**

- Compares **only values**, not types.
- Performs **type coercion** if the types are different.
- Can lead to unexpected results due to automatic conversions.

📌 Example:

```javascript
console.log(5 == "5"); // true (string "5" converted to number)
console.log(0 == false); // true (false converted to 0)
console.log(null == undefined); // true (special rule)
console.log([] == false); // true (empty array converted to "")
```

---

## 2️⃣ **`===` (Strict Equality)**

- Compares **both values and types**.
- No type coercion is performed.
- Safer and more predictable.

📌 Example:

```javascript
console.log(5 === "5"); // false (different types: number vs string)
console.log(0 === false); // false (number vs boolean)
console.log(null === undefined); // false (different types)
console.log(10 === 10); // true (same value and type)
```

---

## 3️⃣ **Comparison Table**

| Operator | Compares       | Type Conversion | Example Result      |
| -------- | -------------- | --------------- | ------------------- |
| `==`     | Values         | ✅ Yes          | `"5" == 5 → true`   |
| `===`    | Values + Types | ❌ No           | `"5" === 5 → false` |

---

## 🧠 Key Takeaways

- Use **`===` (strict equality)** in most cases to avoid unexpected type coercion.
- Use `==` **only when you intentionally want type conversion** (rare in modern code).
- Pair it with **truthy/falsy knowledge** for safer conditions.

---

📌 **Best Practice:**
Always prefer `===` and `!==` in production code.

[🔝 Back to Top](#table-of-contents)

### 6. What is hoisting in JavaScript?

**Hoisting** is JavaScript’s default behavior of moving **variable and function declarations** to the top of their scope (before code execution).

This means you can use variables and functions **before they are declared**, but with some differences between `var`, `let`, `const`, and functions.

---

## 1️⃣ Hoisting with `var`

- `var` declarations are hoisted and **initialized with `undefined`**.
- Accessing them before declaration gives `undefined` instead of an error.

📌 Example:

```javascript
console.log(a); // undefined (hoisted)
var a = 10;
console.log(a); // 10
```

---

## 2️⃣ Hoisting with `let` and `const`

- Declarations are hoisted but **not initialized**.
- They remain in the **Temporal Dead Zone (TDZ)** until the actual line of declaration.
- Accessing them before declaration causes a **ReferenceError**.

📌 Example:

```javascript
// console.log(b); // ❌ ReferenceError
let b = 20;

// console.log(c); // ❌ ReferenceError
const c = 30;
```

---

## 3️⃣ Hoisting with Functions

- **Function Declarations** are fully hoisted, meaning you can call them before defining.
- **Function Expressions** (with `var`, `let`, `const`) are hoisted differently.

📌 Function Declaration:

```javascript
greet(); // ✅ Works (hoisted)

function greet() {
  console.log("Hello from function!");
}
```

📌 Function Expression:

```javascript
// sayHello(); // ❌ TypeError if using var (sayHello is undefined)
// ❌ ReferenceError if using let/const

var sayHello = function () {
  console.log("Hello!");
};
```

---

## 4️⃣ Summary of Hoisting Behavior

| Declaration Type | Hoisted? | Initialized?             | Access before declaration   |
| ---------------- | -------- | ------------------------ | --------------------------- |
| `var`            | ✅ Yes   | `undefined`              | Allowed (returns undefined) |
| `let`            | ✅ Yes   | ❌ No (TDZ)              | ❌ ReferenceError           |
| `const`          | ✅ Yes   | ❌ No (TDZ)              | ❌ ReferenceError           |
| Function Decl.   | ✅ Yes   | ✅ Yes                   | ✅ Allowed                  |
| Function Expr.   | ✅ Yes   | Depends on var/let/const | ❌ Error                    |

---

## 🧠 Key Takeaways

- Hoisting **moves declarations, not initializations**.
- `var` is hoisted with `undefined`, while `let` and `const` are in the TDZ.
- Function declarations are hoisted, but function expressions are not safely usable before definition.

[🔝 Back to Top](#table-of-contents)

### 7. What is the difference between null and undefined?

In JavaScript, both `null` and `undefined` represent the **absence of a value**, but they are used in different contexts and have subtle differences.

---

## 1️⃣ **undefined**

- A variable that has been **declared but not assigned a value** is `undefined`.
- It is the **default value** for:
  - Uninitialized variables
  - Missing function arguments
  - Missing object properties

📌 Example:

```javascript
let a;
console.log(a); // undefined

function greet(name) {
  console.log(name);
}
greet(); // undefined (no argument passed)

let person = {};
console.log(person.age); // undefined (property does not exist)
```

---

## 2️⃣ **null**

- `null` is an **intentional assignment** of "no value".
- It is explicitly set by the programmer to indicate that a variable is **empty** or has **no value**.

📌 Example:

```javascript
let b = null;
console.log(b); // null

let person = { name: "Atikur", age: null };
console.log(person.age); // null (explicitly set)
```

---

## 3️⃣ **Key Differences**

| Feature     | `undefined`                           | `null`                          |
| ----------- | ------------------------------------- | ------------------------------- |
| **Meaning** | Variable declared but not assigned    | Explicit "no value" assignment  |
| **Type**    | `undefined` (primitive type)          | `object` (historical JS bug)    |
| **Default** | Default for uninitialized variables   | Must be manually assigned       |
| **Usage**   | Indicates absence of value implicitly | Indicates intentional emptiness |

---

## 4️⃣ **Comparison Examples**

```javascript
console.log(null == undefined); // true (type coercion)
console.log(null === undefined); // false (different types)

console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object" (quirk in JS)
```

---

## 🧠 Key Takeaways

- `undefined` → JavaScript sets it automatically for uninitialized or missing values.
- `null` → You set it explicitly when you want to say "no value".
- Always use **strict equality (`===`)** to avoid confusion between the two.

[🔝 Back to Top](#table-of-contents)

### 8. What is scope in JavaScript?

**Scope** in JavaScript refers to the **current context of execution** in which values and expressions are visible or can be referenced.

It determines the **accessibility (visibility)** of variables, functions, and objects in different parts of the code.

---

## 1️⃣ **Types of Scope in JavaScript**

### 🔹 Global Scope

- Variables declared **outside any function or block** are in the global scope.
- Accessible from **anywhere in the program**.

```javascript
var globalVar = "I am global";

function show() {
  console.log(globalVar); // Accessible
}
show();
console.log(globalVar); // Accessible
```

---

### 🔹 Function Scope

- Variables declared with `var` inside a function are **function-scoped**.
- They cannot be accessed outside the function.

```javascript
function test() {
  var x = 10;
  console.log(x); // 10
}
test();
// console.log(x); // ❌ ReferenceError (not accessible outside)
```

---

### 🔹 Block Scope (ES6: `let` and `const`)

- Variables declared with `let` or `const` are **block-scoped**.
- Accessible only inside the `{}` block where they are defined.

```javascript
{
  let y = 20;
  const z = 30;
  console.log(y, z); // 20, 30
}
// console.log(y); // ❌ ReferenceError
// console.log(z); // ❌ ReferenceError
```

---

### 🔹 Lexical Scope

- Inner functions have access to variables from **their parent scope**.
- Also known as **static scope**.

```javascript
function outer() {
  let a = "outer";

  function inner() {
    console.log(a); // Accessible due to lexical scope
  }
  inner();
}
outer();
```

---

## 2️⃣ **Scope Chain**

- When trying to access a variable, JavaScript looks in the **current scope**.
- If not found, it looks **outward through parent scopes** until the global scope.
- If still not found, it returns `ReferenceError`.

📌 Example:

```javascript
let global = "global";

function outer() {
  let outerVar = "outer";

  function inner() {
    let innerVar = "inner";
    console.log(global); // ✅ found in global scope
    console.log(outerVar); // ✅ found in outer scope
    console.log(innerVar); // ✅ found in inner scope
  }
  inner();
}
outer();
```

---

## 🧠 Key Takeaways

- **Global scope**: Accessible everywhere.
- **Function scope**: Variables accessible only inside the function (`var`).
- **Block scope**: Variables accessible only inside `{}` (`let`, `const`).
- **Lexical scope**: Inner functions can access variables from parent scopes.
- JavaScript uses a **scope chain** to resolve variable access.

[🔝 Back to Top](#table-of-contents)

### 9. What are closures in JavaScript?

A **closure** is a function that **remembers and accesses variables** from its **outer scope** even after the outer function has finished executing.

Closures are created every time a function is defined inside another function and gives the inner function access to the outer function’s scope.

---

## 1️⃣ **Basic Example**

```javascript
function outer() {
  let count = 0;

  function inner() {
    count++;
    console.log(count);
  }

  return inner;
}

const counter = outer();
counter(); // 1
counter(); // 2
counter(); // 3
```

✅ Here, `inner()` is a closure. It keeps access to the variable `count` from `outer()` even after `outer()` has finished executing.

---

## 2️⃣ **Closures with Parameters**

```javascript
function multiplier(factor) {
  return function (num) {
    return num * factor;
  };
}

const double = multiplier(2);
console.log(double(5)); // 10

const triple = multiplier(3);
console.log(triple(5)); // 15
```

✅ `double` and `triple` are closures that "remember" the value of `factor` from their respective calls.

---

## 3️⃣ **Real-World Uses of Closures**

- **Data privacy & encapsulation** (simulate private variables).
- **Function factories** (create customized functions).
- **Event handlers & callbacks**.
- **Maintaining state** without using global variables.

---

### 🔹 Example: Private Variables

```javascript
function createBankAccount(initialBalance) {
  let balance = initialBalance;

  return {
    deposit(amount) {
      balance += amount;
      return balance;
    },
    withdraw(amount) {
      balance -= amount;
      return balance;
    },
    getBalance() {
      return balance;
    },
  };
}

const account = createBankAccount(100);
console.log(account.deposit(50)); // 150
console.log(account.withdraw(20)); // 130
console.log(account.getBalance()); // 130
```

✅ `balance` is **private** — it can only be accessed through the returned methods, thanks to closures.

---

## 🧠 Key Takeaways

- A **closure** is a function that has access to variables from its outer scope even after that scope has returned.
- Helps in **data privacy, state management, and callbacks**.
- Commonly used in **functional programming** and **event-driven code**.

[🔝 Back to Top](#table-of-contents)

### 10. What is the difference between function declaration and function expression?

In JavaScript, functions can be defined in two main ways: **function declarations** and **function expressions**.  
They look similar but behave differently due to **hoisting** and how they are defined.

---

## 1️⃣ **Function Declaration**

- Defined using the `function` keyword.
- **Hoisted** completely (you can call it before it’s defined in code).
- Named functions.

```javascript
// Function Declaration
function greet() {
  return "Hello!";
}

console.log(greet()); // ✅ "Hello!"
```

✅ This works even if you call `greet()` before its definition because **declarations are hoisted**.

---

## 2️⃣ **Function Expression**

- A function assigned to a variable.
- Can be **anonymous** or named.
- **Not hoisted** the same way — you can only call it after the assignment.

```javascript
// Function Expression
const greet = function () {
  return "Hello!";
};

console.log(greet()); // ✅ "Hello!"
```

❌ If you try `greet()` **before** the definition, you’ll get an error:
`TypeError: greet is not a function`

---

## 3️⃣ **Key Differences**

| Feature                | Function Declaration                   | Function Expression                                    |
| ---------------------- | -------------------------------------- | ------------------------------------------------------ |
| **Hoisting**           | Fully hoisted, can be called earlier   | Not hoisted, must be defined first                     |
| **Syntax**             | `function name() {}`                   | `const name = function() {}`                           |
| **Anonymous Allowed?** | No (must have a name)                  | Yes (can be anonymous or named)                        |
| **When to Use?**       | When defining reusable named functions | When functions are assigned as values or passed around |

---

## 4️⃣ **Example: Hoisting Difference**

```javascript
sayHi(); // ✅ Works (hoisted)
function sayHi() {
  console.log("Hi!");
}

sayHello(); // ❌ Error: Cannot access 'sayHello' before initialization
const sayHello = function () {
  console.log("Hello!");
};
```

---

## 🧠 Key Takeaways

- **Function Declarations** are hoisted, so you can call them before defining.
- **Function Expressions** are not hoisted in the same way — must be defined before use.
- Use **declarations** for global, reusable functions; use **expressions** for inline or callback functions.

[🔝 Back to Top](#table-of-contents)

### 11. What is the event loop in JavaScript?

The **event loop** is a fundamental concept in JavaScript that enables **asynchronous, non-blocking behavior**.  
Since JavaScript is **single-threaded**, it can only do one thing at a time. The event loop allows JavaScript to handle tasks like timers, promises, and I/O operations **without blocking the main thread**.

---

## 1️⃣ **How It Works**

JavaScript runtime consists of three main parts:

1. **Call Stack** → Where functions are executed.
2. **Web APIs (Browser/Node.js APIs)** → Handles async operations (e.g., `setTimeout`, `fetch`).
3. **Callback Queue / Microtask Queue** → Stores async callbacks waiting to run.

The **event loop** continuously checks:

- If the **call stack** is empty.
- If there are tasks in the **microtask queue** (e.g., `Promises`).
- Then pushes them to the call stack for execution.

---

## 2️⃣ **Illustration**

```text
Call Stack   <---->   Event Loop   <---->   Callback Queue
      |                                      (setTimeout, events)
      |
      v
Microtask Queue (Promises, MutationObserver)
```

---

## 3️⃣ **Example with setTimeout**

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout Callback");
}, 0);

console.log("End");
```

**Output:**

```
Start
End
Timeout Callback
```

✅ Even with `0ms` delay, the `setTimeout` callback runs **after** the synchronous code, because the event loop waits for the call stack to be clear.

---

## 4️⃣ **Example with Promises**

```javascript
console.log("Start");

Promise.resolve().then(() => {
  console.log("Promise Callback");
});

console.log("End");
```

**Output:**

```
Start
End
Promise Callback
```

✅ Promise callbacks go into the **microtask queue**, which is processed **before** the callback queue.

---

## 5️⃣ **Key Points**

- JavaScript is **single-threaded** but uses the event loop for concurrency.
- **Call Stack** → executes functions.
- **Microtask Queue** → runs promises and microtasks before the callback queue.
- **Callback Queue** → runs tasks like `setTimeout`, `setInterval`, DOM events.

---

## 🧠 Real-World Analogy

Think of a **restaurant**:

- The **chef** (call stack) cooks one dish at a time.
- **Waiters** (Web APIs) handle orders and timers.
- When a dish is ready, it’s put in a **queue**.
- The **event loop** checks if the chef is free, then gives the next dish to cook.

---

## 📝 Interview Tip

If asked:
👉 _"Why doesn’t setTimeout with 0ms run immediately?"_
Answer: Because it goes to the **callback queue** and only executes after the call stack is empty and microtasks are completed.

---

[🔝 Back to Top](#table-of-contents)

### 12. Explain `call`, `apply`, and `bind` methods in JavaScript

In JavaScript, functions are **first-class objects**, which means they come with built-in methods.  
Three important ones are **`call`**, **`apply`**, and **`bind`**, which allow you to **manually set the value of `this`** when invoking a function.

---

## 1. `call()`

- Invokes the function **immediately**.
- Accepts arguments **individually** (comma-separated).
- Syntax: `func.call(thisArg, arg1, arg2, ...)`

**Example:**

```javascript
function greet(city, country) {
  console.log(`Hello, my name is ${this.name} from ${city}, ${country}`);
}

const person = { name: "Atikur" };

greet.call(person, "Kolkata", "India");
```

**Output:**

```
Hello, my name is Atikur from Kolkata, India
```

---

## 2. `apply()`

- Invokes the function **immediately** (like `call`).
- Accepts arguments **as an array**.
- Syntax: `func.apply(thisArg, [argsArray])`

**Example:**

```javascript
greet.apply(person, ["Delhi", "India"]);
```

**Output:**

```
Hello, my name is Atikur from Delhi, India
```

---

## 3. `bind()`

- **Does not invoke the function immediately**.
- Returns a **new function** with `this` bound to the provided object.
- Syntax: `const boundFunc = func.bind(thisArg, arg1, arg2, ...)`

**Example:**

```javascript
const boundGreet = greet.bind(person, "Mumbai", "India");
boundGreet(); // Executes later
```

**Output:**

```
Hello, my name is Atikur from Mumbai, India
```

---

## 4. Key Differences

| Method  | Invokes Immediately? | Argument Passing                         |
| ------- | -------------------- | ---------------------------------------- |
| `call`  | Yes                  | Comma-separated                          |
| `apply` | Yes                  | Array of args                            |
| `bind`  | No                   | Returns new function (can pass args too) |

---

## 5. Use Cases

- **`call`** → Borrowing methods from one object to use on another.
- **`apply`** → Similar to `call`, but useful when arguments are already in an array (e.g., `Math.max.apply(null, arr)`).
- **`bind`** → When you want to **fix `this`** for later use (e.g., in event listeners, callbacks).

---

[🔝 Back to Top](#table-of-contents)

### 13. What are Arrow Functions and How Are They Different?

Arrow functions, introduced in **ES6 (ECMAScript 2015)**, are a **shorter syntax** for writing functions in JavaScript.  
They are especially useful for writing concise code and handling the `this` keyword differently than traditional functions.

---

## 1. Syntax

```javascript
// Traditional function
function add(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;
```

- If the function body has only **one expression**, the `return` keyword and curly braces `{}` can be omitted.
- If there is only **one parameter**, parentheses `()` are optional:

```javascript
const square = (x) => x * x;
```

---

## 2. Key Differences Between Arrow Functions and Regular Functions

| Feature                | Regular Function                             | Arrow Function                                                  |
| ---------------------- | -------------------------------------------- | --------------------------------------------------------------- |
| **Syntax**             | Verbose (`function` keyword required)        | Short and concise (`=>`)                                        |
| **`this` binding**     | `this` depends on how the function is called | `this` is **lexically bound** (inherits from surrounding scope) |
| **`arguments` object** | Has its own `arguments` object               | Does **not** have its own `arguments`                           |
| **`new` keyword**      | Can be used as a constructor                 | Cannot be used as a constructor                                 |
| **Methods in objects** | Suitable for defining object methods         | Not suitable (because of `this` binding)                        |

---

## 3. Example: `this` Behavior

### Regular Function

```javascript
const person = {
  name: "Atikur",
  greet: function () {
    console.log(`Hello, my name is ${this.name}`);
  },
};

person.greet(); // "Hello, my name is Atikur"
```

### Arrow Function

```javascript
const person = {
  name: "Atikur",
  greet: () => {
    console.log(`Hello, my name is ${this.name}`);
  },
};

person.greet(); // "Hello, my name is undefined" (because arrow inherits `this` from outer scope)
```

---

## 4. Use Cases

- Best for **callbacks** (e.g., `map`, `filter`, `forEach`) where we don’t want to re-bind `this`.
- Not suitable for **object methods** or **constructors**.

---

[🔝 Back to Top](#table-of-contents)

### 14. What is the Difference Between Synchronous and Asynchronous Code?

---

## 1. Synchronous Code

- Code is executed **line by line** in a sequence.
- Each operation **blocks** the execution of the next one until it is completed.
- If a task takes time (e.g., a network call), it **freezes** the program until it finishes.

**Example:**

```javascript
console.log("Start");

function task() {
  for (let i = 0; i < 1e9; i++) {} // long-running task
  console.log("Task finished");
}

task();
console.log("End");

// Output:
// Start
// Task finished
// End
```

Here, the long-running loop **blocks** the execution, so `"End"` is printed only after the task is complete.

---

## 2. Asynchronous Code

- Code does **not block** the execution of the next operation.
- Long-running tasks are handled in the **background** (via callbacks, promises, or async/await).
- Common for tasks like **API requests, timers, file I/O, and database queries**.

**Example with `setTimeout`:**

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Task finished (after 2s)");
}, 2000);

console.log("End");

// Output:
// Start
// End
// Task finished (after 2s)
```

Here, the program continues execution without waiting for `setTimeout` to complete.

---

## 3. Key Differences

| Feature         | Synchronous                     | Asynchronous                            |
| --------------- | ------------------------------- | --------------------------------------- |
| **Execution**   | Line by line, in order          | Non-blocking, can continue other tasks  |
| **Performance** | Slower if tasks take time       | Faster for long tasks (uses event loop) |
| **Use Case**    | Simple operations, calculations | API calls, timers, file/database I/O    |

---

## 4. Modern Asynchronous Patterns

- **Callbacks**
- **Promises**
- **Async/Await**

Example using `async/await`:

```javascript
async function fetchData() {
  console.log("Fetching data...");
  const data = await new Promise((resolve) =>
    setTimeout(() => resolve("Data loaded"), 2000)
  );
  console.log(data);
}

fetchData();
console.log("End");

// Output:
// Fetching data...
// End
// Data loaded (after 2s)
```

---

[🔝 Back to Top](#table-of-contents)
