---
layout: post
title:  "How to create a class in JavaScript"
date:   2017-03-22 06:35:48 -0700
categories: OOP javascript
---

In JavaScript classes can be created using functions. Let's see how.

{% highlight javascript %}

function Car() {
    this.make = 'Honda';
    this.model = 'Civic';
    this.color = 'gray';

    this.getInfo = function() {
        return this.make + ' ' + this.model + ' ' + this.color;
    };
}

{% endhighlight %}

{% highlight javascript %}

var mycar = new Car();

{% endhighlight %}

The method getInfo() gets recreated every time we create a new object. Instead
we can add getInfo() to the prototype.

{% highlight javascript %}
Car.prototype.getInfo = function() {
    return this.make + ' ' + this.model + ' ' + this.color;
}
{% endhighlight %}
