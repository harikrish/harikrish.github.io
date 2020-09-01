---
layout: post
title: Javascript Object oriented programming
categories: [JavaScript, Programming]
---

*JavaScript is a prototype-based language which contains no class statement. Instead JavaScript uses functions as classes. Defining a class is as easy as defining a function.

	
*An object constructor/object constructor function is a function that’s used to define a new object. In this function, we declare the initial properties/methods of the new object, and usually assign them a pre-defined value.

	
*To create an instance of an object, we use the keyword "new", followed by an object constructor. We can either use JavaScript’s built-in constructors to create a native object, or we can build our own constructors to create a user-defined object.

	
*Every object method has a variable – this – which refers to the current instance of that object from which the method is called.
Example

{% highlight javascript %}
function Computer(name) {
      this.name=name;
      this.getName=function() {
         return this.name;
      }
}

var computer1 = new Computer("Desktop-1");
alert(computer1.getName());//alerts Desktop-1
var computer2 = new Computer("Desktop-2");
alert(computer2.getName());//alerts Desktop-2
{% endhighlight %}

### References
- [http://www.sitepoint.com/oriented-programming-1/](http://www.sitepoint.com/oriented-programming-1/)
- [https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript](https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript)