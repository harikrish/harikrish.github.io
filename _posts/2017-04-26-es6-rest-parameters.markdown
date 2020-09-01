---
layout: post
title:  "ES6 Rest parameters"
date:   2017-04-26 15:03:00 -0700
categories: [ES6, JavaScript]
---

The rest parameter syntax allows us to represent an indefinite number of arguments
as an array.
If you prefix a parameter name with the rest operator (...), the parameter receives
all remaining parameters via an Array.
Only the last parameter can be a "rest parameter".
This syntax was introduced in ECMAScript 2015(commonly called as ES6).

{% highlight javascript %}
function foo(a, b, ...moreArgs) {
    console.log(a); //1
    console.log(b); //2
    console.log(moreArgs); //[3, 4, 5, 6, 7]
}

foo(1, 2, 3, 4, 5, 6, 7);
{% endhighlight %}

### References
- [Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)