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
**Short answer:** A Promise represents a future value: pending → fulfilled or rejected.

**Deep dive:** 

### Difference between `Promise.all` vs `Promise.allSettled`, vs ``
**Short answer:**
- `Promise.all`: fails fast if any promise rejects
- `Promise.allSettled`: waits for all results (fulfilled/rejected)
- `const`: binding cannot be reassigned (object contents can still mutate)

**Example:**
```js

```
