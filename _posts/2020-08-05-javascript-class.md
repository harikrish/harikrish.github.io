---
layout: post
title:  "JavaScript Classes"
date:   2020-08-05 10:47:00 -0700
categories: [JavaScript, ES6]
---

JavaScript classes were introduced in ECMAScript 2015(ES6). They are 
primarily syntactical sugar over JavaScript's existing prototype based inheritance.

{% highlight javascript %}
class Rectangle {
    constructor(width, height) {
        this.width = width;
        this.height = height;
    }

    area() {
        return (this.width * this.height);
    }
}
{% endhighlight %}

The `constructor` method is a special method for creating and initializing an object created with a class.

A `constructor` can use the `super` keyword to call the constructor of the super class.

Sub classes can be created with `extends` keyword.

{% highlight javascript %}
class Square extends Rectangle {
    constructor(width, height) {
        super(width, height);
    }

    area() {
        let result = super.area();
        console.log("Area of square is ", result);
    }
}
{% endhighlight %}


### References
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)