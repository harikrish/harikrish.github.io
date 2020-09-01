---
layout: post
title:  "JavaScript Object"
date:   2020-08-24 10:24:00 -0700
categories: [JavaScript]
---

An object is a collection of properties. A property is a associate between  a name
and a value.

`for...in` can be used to iterate over all the enumerable properties of an object.

{% highlight javascript %}
var myFan = {
    make: 'Honeywell',
    blades: 4,
    rotation: 'on'
}

for (var i in myFan) {
    if (myFan.hasOwnProperty(i)) {
        console.log(i + " :: " + myFan[i]);
    }
}
// outputs
// make :: Honeywell
// blades :: 4
// rotation :: on
{% endhighlight %}

### Ways to create objects
#### Object initializers
{% highlight javascript %}
var rectangle = {width: 10, height: 100};
{% endhighlight %}

#### Constructor function
{% highlight javascript %}
function TV(make, model) {
    this.make = make;
    this.model = model;
}

var myTv = new TV('LG', 'ThinQ');
{% endhighlight %}

#### Object.create
Allows to choose the prototype object for the object you want to create, 
without having to define a constructor function.
{% highlight javascript %}
var bike = {
    wheels : 2,
    gear: 6
}
var myBike = Object.create(bike);
{% endhighlight %}

### References:
- [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [Working with Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
- [Details of the object model](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model)