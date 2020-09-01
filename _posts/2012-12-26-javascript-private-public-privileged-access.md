---
layout: post
title: JavaScript private public privileged access
categories: [JavaScript, Programming]
---

### Public

The members of an object are all public members. There are two ways for putting members in a new object.

In Constructor

{% highlight javascript %}
function Container(param) {
    this.member = param;
}
{% endhighlight %}

In the prototype

This technique is used to add public methods.

{% highlight javascript %}
Container.prototype.stamp = function (string) {
    return this.member + string;
}
{% endhighlight %}

### Private

Private members are made by the constructor. Ordinary vars and parameters of the constructor become the private members.

{% highlight javascript %}
function Container(param) {
    this.member = param;
    var secret = 3;
    var that = this;
}
{% endhighlight %}

### Privileged

A privileged method is able to access private methods, variables and is itself accessible to the public method and the outside.  Privileged methods are assigned with "this" within the constructor.

{% highlight javascript %}
function Container(param) {
    this.member = param;

    this.service = function () {
        return this.member;
    };
}
{% endhighlight %}
 
### References:
- [http://javascript.crockford.com/private.html](http://javascript.crockford.com/private.html)
- [http://phrogz.net/JS/classes/OOPinJS.html](http://phrogz.net/JS/classes/OOPinJS.html)
- [https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Inheritance_and_the_prototype_chain](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Inheritance_and_the_prototype_chain)
- [https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript](https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript)