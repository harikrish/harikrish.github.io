---
layout: post
title:  "ES6 Spread Syntax"
date:   2017-04-25 17:13:00 -0700
categories: [ES6, JavaScript]
---

The spread syntax allows an expression to be expanded in places where multiple arguments
(for function calls) or multiple elements (for array literals) or multiple variables
(for destructuring assignments) are expected.

Spread syntax can be only applied to iterable objects.

Rest syntax looks exactly like spread syntax. In a way, rest syntax is the opposite of spread syntax. Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element.

{% highlight javascript %}

function sum(a, b) {
    return a+b;
}

const args = [1, 2];

let result = sum(...args); 
console.log(result); // 3

{% endhighlight %}

{% highlight javascript %}

const arr = [1, 2, 3];
const arrCopy = [...arr]; 
console.log(arrCopy); // [1, 2, 3]
{% endhighlight %}

### References
- [Spread syntax (...)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator)
- [ES6 Spread and Butter in Depth](https://ponyfoo.com/articles/es6-spread-and-butter-in-depth)