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
10. [What is the difference between function declaration and expression?](#10-what-is-the-difference-between-function-declaration-and-expression)

### 🟡 Intermediate Level

11. [What is the event loop in JavaScript?](#11-what-is-the-event-loop-in-javascript)
12. [Explain call, apply, and bind methods.](#12-explain-call-apply-and-bind-methods)
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
