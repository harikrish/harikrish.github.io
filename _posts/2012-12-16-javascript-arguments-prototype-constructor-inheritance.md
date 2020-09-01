---
layout: post
title: JavaScript Arguments, Prototype, Constructor, Inheritance
categories: JavaScript
---

### Arguments

In every JavaScript function a private variable argument is automatically created, holding array of the arguments passed to the function.

### Prototype

Every object has a special property, prototype. This property allows you to add properties/methods to all objects created from that object constructor. The prototype object loads before the object constructor does anything. Therefore by using prototype we can add properties, methods to both native objects and user-defined objects.

### Constructor

Every instance of an object has a constructor property. It returns the Function object that created that instance of the object.

### Inheritance

The 
prototype property is an object with no initial properties/methods. When we add properties/methods to this object, we automatically add them to all instances of the object. However, instead of adding properties/methods to the 
prototype object, we could replace the prototype object with an object that already has the properties/methods we want.

### References
- [JavaScript Object-Oriented Programming Part 2 Article](http://www.sitepoint.com/oriented-programming-2/)
- [Introducing JavaScript objects](https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript)