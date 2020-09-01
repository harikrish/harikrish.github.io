---
layout: post
title:  "ES6 Destructuring"
date:   2017-04-26 17:09:00 -0700
categories: [ES6, JavaScript]
---

Destructuring assignment allows you to assign the properties of an array
or object to variables using syntax that looks similar to array or object
literals. This syntax can be extremely terse, while still exhibiting
more clarity than the traditional property access.
This new syntax was introduced in ECMAScript 2015 (ES6).

{% highlight javascript %}
// Array destructuring
let arr = [1, 2, 3];
let [a, b, c] = arr;
console.log(a); // 1
console.log(b); // 2
console.log(c); // 3

// Object destructuring
let obj = {
    x: 1,
    y: 2
}

let {x, y} = obj;
console.log(x); //1
console.log(y); //2
{% endhighlight %}


References
- [ES6 In Depth: Destructuring](https://hacks.mozilla.org/2015/05/es6-in-depth-destructuring/)
- [Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)