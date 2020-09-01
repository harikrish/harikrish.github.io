---
layout: post
title:  "JavaScript Iterators"
date:   2020-08-12 14:26:00 -0700
categories: [JavaScript, ES6]
---

JavaScript Iterators were added in ECMAScript 2015(ES6).
It allows JavaScript objects to specify how custom objects can be used
in `for...of` loops.
For a object to be `iterable` it must implement `iteratorMethod`.
When object needs to be iterated is `iteratorMethod` is called
with no arguments. The `iteratorMethod` returns a `iterator`.
The object must have a property which is available via a constant `Symbol.Iterator`.
The value of the property must be the `iterator` method.
An object is a `iterator` if it has a `next` function which is a zero
argument function that returns a object with atleast two properties
`done(boolean)` - Has value `true` when the iterator has completed its sequence.
Has value `false` if the iterator was able to produce next value in the sequence.
`value` - Any JavaScript value returned by the iterator.

{% highlight javascript %}

let fooIterator = {
    next: function() {
        if (this.counter < 10) {
            this.counter ++;
            return { value: this.counter, done: false };
        }
        return { value: undefined, done: true };
    },
    counter: 0,
    [Symbol.iterator]: function() {
        return this;
    }
}

for (let value of fooIterator) {
    console.log(value); // 1 2 3 4 5 6 7 8 9 10
}

{% endhighlight %}

### References
- [A Simple Guide to ES6 Iterators in JavaScript with Examples](https://codeburst.io/a-simple-guide-to-es6-iterators-in-javascript-with-examples-189d052c3d8e)
- [Iteration protocols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols)