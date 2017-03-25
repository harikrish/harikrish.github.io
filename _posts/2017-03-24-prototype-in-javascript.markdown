---
layout: post
title:  "What is prototype and prototype chain in JavaScript"
date:   2017-03-24 07:03:48 -0700
categories: OOP javascript
---

Each JavaScript object has a private property which holds a
link to another object called its prototype. That prototype
object has a prototype of its own, and so on until a object
is reached with null as its prototype. null has no prototype
and acts as the final link in this prototype chain.
