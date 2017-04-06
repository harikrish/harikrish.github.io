---
layout: post
title:  "ES6 Arrow functions"
date:   2017-04-22-5 17:00:10 -0700
categories: ES6 JavaScript
---

Arrow functions are a more concise syntax for writing function expressions.

Advantages of Arrow functions
- More concise
- Arrow functions do not create its own this context. so 'this' has it
original meaning from the enclosing context.

Things to watch out for when using Arrow functions
- call, apply, bind do not change the value of this in Arrow functions.
- Arrow functions cannot be used as constructors
- Arrow functions cannot be used as generators.
- Arrow functions do not have the local variable 'arguments' as do other
functions.

References
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions
- https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript/
