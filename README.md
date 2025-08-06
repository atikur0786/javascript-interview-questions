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

## 📚 Table of Contents

### 🟢 Beginner Level (Fundamentals)

1. [What is JavaScript and how is it different from Java?](#1-what-is-javascript-and-how-is-it-different-from-java)
2. [Explain var, let, and const with examples.](#2-explain-var-let-and-const-with-examples)
3. [What are data types in JavaScript?](#3-what-are-data-types-in-javascript)
4. [What are truthy and falsy values?](#4-what-are-truthy-and-falsy-values)
5. [Explain == vs ===.](#5-explain--vs-)
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

[🔝 Back to Top](#table-of-contents)
