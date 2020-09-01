---
layout: post
title:  "Different ways of creating Objects in JavaScript"
date:   2017-03-25 09:47:39 -0700
categories: JavaScript
---

Explained below are some of the different ways of creating
Objects in JavaScript. 

- Objects created with syntax constructs (Object Literal Notation)

{% highlight javascript %}

var o = {a: 1};

{% endhighlight %}

- With Function (New Objects with Constructor function)

A constructor is a function that contains instructions about the properties of an object when that object is created and assigned. Advantage over object literal is you can create many instances of objects that have the same properties.

{% highlight javascript %}

function Car() {
    this.make = 'Honda';
    this.model = 'Civic';
}

var c = new Car();

{% endhighlight %}

- With Object.create

ECMAScript 5 introduced a new method Object.create.

{% highlight javascript %}

var a = {a: 1};

var b = Object.create(a);

console.log(b.a); // 1 (inherited)

{% endhighlight %}

- With Class

JavaScript classes were introduced in ECAMScript 2015 (ES6)

{% highlight javascript %}

Class Car {
    constructor(make, model) {
        this.make = make;
        this.model = model;
    }
}

var c = new Car();

{% endhighlight %}

### Reference
- [Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain#With_Object.create)
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
