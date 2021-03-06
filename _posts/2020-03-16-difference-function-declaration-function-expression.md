---
layout: post
title:  "Difference between function declaration and function expression"
date:   2020-03-16 06:17:48 -0700
categories: JavaScript
---

Function declarations are hoisted to the top of the code by the browser before any code is executed. Specifically, all of the functions written with function declarations are “known” before any code is run. This allows you to call a function before you declare.

Function expressions, however, do not hoist. If you try to run a function before you’ve expressed it, you’ll get an error.

### References
- [Function expressions vs. function declarations](https://gomakethings.com/function-expressions-vs-function-declarations/)
- [Understanding Hoisting in JavaScript](https://scotch.io/tutorials/understanding-hoisting-in-javascript)