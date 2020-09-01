---
layout: post
title:  "JavaScript Generators"
date:   2020-08-12 14:26:00 -0700
categories: [JavaScript, ES6]
---

Generator functions , allow you to define a function 
whose execution is not continuous. Generator functions
are written using the `function*` syntax.

Generator function do not initially execute their code.
Instead they return a special type of iterator called 
a Generator. When a value is consumed by calling the 
generators `next` method, then function executes until
it encounters `yield` keyword.


{% highlight javascript %}
function* fooGenerator() {
    yield 1;
    yield 2;
    yield 3;
}

for (const val of fooGenerator()) {
    console.log(val); // 1 2 3
}
{% endhighlight %}


### References:
- [Iterators and generators
](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators)
- [Understanding Generators in ES6 JavaScript with Examples](https://codeburst.io/understanding-generators-in-es6-javascript-with-examples-6728834016d5)