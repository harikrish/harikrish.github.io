---
layout: post
title:  "What is prototype and prototype chain in JavaScript"
date:   2017-03-24 07:03:48 -0700
categories: JavaScript
---

Each JavaScript object has a private property which holds a
link to another object called its prototype. That prototype
object has a prototype of its own, and so on until a object
is reached with null as its prototype. null has no prototype
and acts as the final link in this prototype chain.

Multiple inheritance with prototypes is referred to as a 
prototype chain.

{% highlight javascript %}
function Car() {
    this.make = "Honda";
    this.model = "Civic";
}

let c = new Car();
Car.prototype.fuel = "Gas";

console.log(c.make); // "Honda"
console.log(c.model); // "Civic"
console.log(c.fuel); // "Gas"
{% endhighlight %}

To check whether an object has a property defined on itself
and not somewhere on its prototype chain, it is necessary to use the
`hasOwnProperty` method which all objects inherit from `Object.prototype`.

{% highlight javascript %}
c.hasOwnProperty("make"); //true
c.hasOwnProperty("fuel"); //false
{% endhighlight %}


### References:
- [Inheritance and the prototype chain
](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- [Prototypal inheritance
](https://javascript.info/prototype-inheritance)