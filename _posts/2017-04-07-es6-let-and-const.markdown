---
layout: post
title:  "let and const in ES6"
date:   2017-04-07 10:00:25 -0700
categories: JavaScript ES6
---

let

let is the new var.
let could be used to declare variables, just like var.

Differences between let and var are
- let variables are block scoped.
- Global let variables are not properties on the global object.
- Loops of the form for (let x...) create a fresh binding for x
in each iteration.
- It's an to try to use a let variable before its declaration
is reached.
- Redeclaring a variable with let is a SyntaxError.


const

Variables declared with const are like let except you can't assign
to them, except at the point where they are declared.
The const declaration creates a read-only reference to a value.
It does not mean the value it holds is immutable, just that the
variable identifier cannot be reassigned.


References

- https://hacks.mozilla.org/2015/07/es6-in-depth-let-and-const/

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const
