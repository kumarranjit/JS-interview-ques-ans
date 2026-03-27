# JavaScript Interview Questions & Answers

A curated set of JavaScript interview questions with concise answers, deeper explanations, and runnable code examples.

## Table of Contents
- [Basics](#basics)
  - [What is JavaScript?](#what-is-javascript)
  - [Difference between `var`, `let`, and `const`](#difference-between-var-let-and-const)
  - [Explain `==` vs `===`](#explain--vs-)
- [Closures](#closures)
  - [What is a closure?](#what-is-a-closure)
- [Promises](#promises)
  - [What is a Promise?](#what-is-a-promise)
  - [`Promise.all` vs `Promise.allSettled`](#promiseall-vs-promiseallsettled)

---

## Basics

### What is JavaScript?
**Short answer:** JavaScript is a single-threaded, garbage-collected language commonly used for web development; it can run in browsers and on servers (Node.js).

**Deep dive:** Explain runtime, event loop, JIT, etc.

### Difference between `var`, `let`, and `const`
**Short answer:**
- `var`: function-scoped, hoisted (initialized as `undefined`)
- `let`/`const`: block-scoped, hoisted but in TDZ
- `const`: binding cannot be reassigned (object contents can still mutate)

**Example:**
```js
console.log(a); // => undefined
var a = 1;

// console.log(b); // ReferenceError (TDZ)
let b = 2;
```
## Closures

### What is a closure?
**Short answer:** A closure is when a function “remembers” variables from its outer scope even after that outer function has returned..

**Example:**
```js
function makeCounter() {
  let count = 0;
  return function () {
    count += 1;
    return count;
  };
}

const counter = makeCounter();
counter(); // 1
counter(); // 2
```
## Promises

### What is a Promise??
**Short answer:** A Promise is a JavaScript object that represents the eventual result (success or failure) of an asynchronous operation.

A Promise can be in three states:
  Pending -> operation is still running
  Fulfilled -> operation completed successfully
  Rejected -> operation failed
Once fulfilled or rejected, the state cannot change.

**Why Do We Need Promises in JavaScript?**
Promises handle asynchronous operations JavaScript runs on a single thread, 
so long operations (API calls, timers, file access) must be handled asynchronously.

**How Promises Help**

  1️⃣ Avoid Callback Hell
  2️⃣ Better Error Handling
  3️⃣ Easier Async Flow Control
  4️⃣ Improves Readability & Maintainability
  
**Deep dive:** 

Promises represents the completion of an asynchronous operation with its result. 
Promises handle single event, It can be success or failure but eventually completed.
Unless the current excution of the event loop is completed(success or failure) callback will never be called before it.
Callback added with 'then()' as after success or failure of the asynchronous operation, 
Callback function take two arguments resolve, reject.
multiple callback may be added each callback is executed one after another in the order which they were inherited.

**Final Summary:**

Promises handle async operations
They replace messy callbacks
Foundation for async/await
Promises handle single event, It can be success or failure but eventually completed.

**Example:**
```js
const promiseFun = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('Data loaded');
  }, 1000);
});

promiseFun
  .then(result => console.log(result))
  .catch(error => console.error(error));
```

### Difference between `Promise.all` vs `Promise.allSettled`, vs ``
**Short answer:**
- `Promise.all`: fails fast if any promise rejects
- `Promise.allSettled`: waits for all results (fulfilled/rejected)
- `const`: binding cannot be reassigned (object contents can still mutate)

**Example:**
```js

```
