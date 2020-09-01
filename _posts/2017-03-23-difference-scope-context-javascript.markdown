---
layout: post
title:  "Difference between scope and context in JavaScript"
date:   2017-03-23 06:51:40 -0700
categories: JavaScript
---

Difference is scope is function based and context is object based.

### Scope 

Variables can have either local or global scope.
Local variables exist only within the function in which they are defined.
Variable declared outside the function can be accessed and modified
by another function also.

{% highlight javascript %}
var planet = "sun"; // global variable

console.log(planet); //sun
{% endhighlight %}

{% highlight javascript %}
function solar_system() {
    var star = "sun"; // local variable
}
console.log(star); // Error, star is not defined
{% endhighlight %}

### Context 
Context `this` is set to the object the function is called on.

{% highlight javascript %}
var myObj = {
    id: 10,
    myFunc: function() {
        console.log(this.id); // this refers to `myObj`
    }
};

myObj.myFunc(); // 10
{% endhighlight %}

{% highlight javascript %}
function foo() {
    console.log(this); // `this` refers to the `window` object
}

foo();  
{% endhighlight %}


### Reference
- [JavaScript Scope and Closures](https://css-tricks.com/javascript-scope-closures/)
- [Understanding Scope and Context in JavaScript](http://ryanmorr.com/understanding-scope-and-context-in-javascript/)

