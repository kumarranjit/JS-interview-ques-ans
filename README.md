# JavaScript Interview Questions & Answers

A curated set of JavaScript interview questions with concise answers, deeper explanations, and runnable code examples.

## How to use this repo
- Skim the **Short answer** first, then read the **Deep dive**.
- Try to predict outputs before running examples.
- Use your editor search (Ctrl/Cmd+F) to find a topic fast.

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
