---
layout: post
title:  "JavaScript interview questions"
date:   2020-06-08 12:47:00 -0700
categories: JavaScript
---

### What's the difference between == and === ?

Double equals (==) will perform a type conversion when comparing two things.
Triple equals (===) will do the same comparison as double equals but without type conversion; if the types differ, false is returned.

### What does the !! operator do ?

Converts Object to boolean. If it was falsey (e.g. 0, null, undefined, etc.), it will be false, otherwise, true.
So !! is not an operator, it's just the ! operator twice.

### What is Hoisting ?

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

### What is Scope ?

Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime. In other words, scope determines the visibility of variables and other resources in areas of your code.

### What are Closures ?

Closures are function which 'remember' the environment in which they were created.
A closure is a combination of a function and the lexical environment within which the function was declared.
This environment consists of any local variables that were in-scope at the time closure was created.

### What are truthy and falsy values ?

A truthy value is a value that is considered  true when evaluated in a Boolean context.
A falsy value is a value that translates to false when evaluated in a Boolean context.
All values are truthy unless they are defined as falsy (i.e., except for false, 0, "", null, undefined, and NaN).

### What does "use strict" do ?

JavaScript's strict mode, introduced in ECMAScript 5, is a way to opt in to a restricted variant of JavaScript.

Strict mode makes several changes to normal JavaScript semantics:
- Eliminates some JavaScript silent errors by changing them to throw errors.
- Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.
- Prohibits some syntax likely to be defined in future versions of ECMAScript.

### What's the value of "this" in JavaScript ?

In JavaScript this always refers to the “owner” of the function we're executing, or rather, to the object that a function is a method of.

### What is the prototype of an object ?

Prototypes are the mechanism by which JavaScript objects inherit features from one another.
JavaScript is often described as a prototype-based language — to provide inheritance, objects can have a prototype object, which acts as a template object that it inherits methods and properties from.
An object's prototype object may also have a prototype object, which it inherits methods and properties from, and so on. This is often referred to as a prototype chain, and explains why different objects have properties and methods defined on other objects available to them.

### What is an IIFE, what is the use of it ?

An IIFE or Immediately Invoked Function Expression is a function that is gonna get invoked or executed after its creation or declaration. The syntax for creating IIFE is that we wrap the function (){} inside a parentheses () or the Grouping Operator to treat the function as an expression and after that we invoke it with another parentheses ().
An Immediately-Invoked Function Expression can be used to “lock in” values and effectively save state.

### What is the use Function.prototype.apply and Function.prototype.call method ?

Every JavaScript function is equipped with "apply" method that allows you to call the function with specific binding. I takes two arguments, the binding object and an array of arguments to be passed to the function.
"Call" method is similar to "apply", but it takes the arguments themselves not an array.

### What is the usage of Function.prototype.bind ?

In JavaScript, binding is always explicit, and can be easily lost, so a method using "this" will not refer to the proper object in all situations,  unless you force it to.
JavaScript provides two options to do explicit binding "apply" and "call".

### What are Higher Order Functions ?

Functions that operate on other functions, either by taking them as arguments or by returing them, are called higher order functions.

### What are first-class functions ?

A programming language is said to have first-class functions if it supports passing functions as arguments to other functions, returning them as the values from other functions, and assigning them to variables or storing them in data strucures.

### What is the arguments object ?

In every JavaScript function a private variable argument is automatically created, holding array of the arguments passed to the function.

### What's the difference between var, let and const keywords ?

`let` could be used to declare variables, just like var. `let` variables are block scoped.
Variables declared with `const` are like let except you can't assign
to them, except at the point where they are declared.
Variables declared with `var` keyword are function scoped.

### What are Arrow functions ?

Arrow functions are a more concise syntax for writing function expressions.



References:
- [70 JavaScript Interview Questions](https://dev.to/macmacky/70-javascript-interview-questions-5gfi)
- [10 Interview Questions Every JavaScript Developer Should Know](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)
- [123-JavaScript-Interview-Questions](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions)
- [JavaScript Questions](https://h5bp.org/Front-end-Developer-Interview-Questions/questions/javascript-questions/)
- [JS: Interview Algorithm](http://thatjsdude.com/interview/js1.html)
- [JS: Basics and Tricky Questions](http://thatjsdude.com/interview/js2.html)
- [The Best Frontend JavaScript Interview Questions](https://performancejs.com/post/hde6d32/The-Best-Frontend-JavaScript-Interview-Questions-(Written-by-a-Frontend-Engineer))
- [Front End Interview Handbook](https://github.com/yangshun/front-end-interview-handbook)
- [Equality comparisons and sameness
](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)
- [What is the !! (not not) operator in JavaScript?](https://stackoverflow.com/questions/784929/what-is-the-not-not-operator-in-javascript)
- [Understanding Scope in JavaScript
](https://scotch.io/tutorials/understanding-scope-in-javascript)
- [Strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
- [Object prototypes](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)