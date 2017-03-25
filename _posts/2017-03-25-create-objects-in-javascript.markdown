---
layout: post
title:  "Different ways of creating Objects in JavaScript"
date:   2017-03-25 09:47:39 -0700
categories: OOP javascript
---

- Objects created with syntax constructs

{% highlight javascript %}

var o = {a: 1};

{% endhighlight %}

- With Function

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

- Reference

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain#With_Object.create
