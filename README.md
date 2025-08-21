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
