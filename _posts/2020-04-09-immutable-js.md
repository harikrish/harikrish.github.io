---
layout: post
title:  "Immutable JS"
date:   2020-04-09 14:42:48 -0700
categories: OOP javascript
---

Much of what makes application development difficult is tracking mutation and maintaining state.
Immutability means that once you call that data structure in being, you can’t make changes to (a.k.a. mutate) the data structure and the data it contains at that particular memory location. 

In Javascript, we have both immutable and mutable data structures.
In JavaScript, strings and numbers are immutable by design.
Examples of native JavaScript values that are mutable include objects, arrays, functions, classes, sets, and maps.

{% highlight javascript %}
// Code from https://benmccormick.org/2016/06/04/what-are-mutable-and-immutable-data-structures-2
let a = 'test';
let b = a;
a = a.substring(2);

console.log(a) //st
console.log(b) //test
console.log(a === b) //false

{% endhighlight %}

{% highlight javascript %}
// Code from https://benmccormick.org/2016/06/04/what-are-mutable-and-immutable-data-structures-2
let a = {
    foo: 'bar'
};

let b = a;

a.foo = 'test';

console.log(b.foo); // test
console.log(a === b) // true

{% endhighlight %}

Benefits of Immutablity : Easier to Debug, Persistence, Easier Deep Value Comparisons, Concurrency

References:
- https://immutable-js.github.io/immutable-js/
- https://medium.com/@yej.arin.choi/this-is-a-post-that-summarizes-my-dive-into-immutability-in-programming-what-it-is-why-its-34cbba44f889
- https://www.sitepoint.com/immutability-javascript/
- https://developer.mozilla.org/en-US/docs/Glossary/Mutable
- https://benmccormick.org/2016/06/04/what-are-mutable-and-immutable-data-structures-2