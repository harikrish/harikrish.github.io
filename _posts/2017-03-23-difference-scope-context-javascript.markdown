---
layout: post
title:  "Difference between scope and context in JavaScript"
date:   2017-03-23 06:51:40 -0700
categories: javascript
---


Difference is scope is function based and context is object based.


- Scope - Variables can have either local or global scope.
Local variables exist only within the function in which they are defined.
Variable declared outside the function can be accessed and modified
by another function also.

- Context - Context 'this' is set to the object the function is called on.
