---
layout: post
title:  "JavaScript Closures"
date:   2017-04-10 11:01:25 -0700
categories: JavaScript
---

Closures are function which 'remember' the environment in which
they were created.
A closure is a combination of a function and the lexical
environment within which the function was declared.
This environment consists of any local variables that were
in-scope at the time closure was created.

The word lexical refers to the fact that lexical scoping uses the location 
where a variable is declared within the source code to determine where that variable 
is available. Nested functions have access to variables declared in their outer scope.

{% highlight javascript %}
function foo() {
    var i = 10;

    function print() {
        console.log(i);
    }

    return print;
}

var printFunc = foo();
printFunc(); // 10
{% endhighlight %}

Common mistake of using closure in for loops
{% highlight javascript %}
for (var x = 0; x < 10; x++) {
    setTimeout(function() {
        console.log(x);
    }, 10);
}
// prints 10, 10 times
{% endhighlight %}

Solution, is to use a function factory
{% highlight javascript %}
function myFunc(p) {
    return function() {
        console.log(p);
    }
}

for (var x = 0; x < 10; x++) {
    setTimeout(myFunc(x), 10);
}
// prints 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
{% endhighlight %}

### References
- [Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
- [JavaScript Closures Demystified](https://www.sitepoint.com/javascript-closures-demystified/)
- [JavaScript Closures Explained](https://lostechies.com/derekgreer/2012/02/17/javascript-closures-explained/)
