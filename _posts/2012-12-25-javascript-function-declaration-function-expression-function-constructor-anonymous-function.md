---
layout: post
title: JavaScript function declaration, function expression, Function constructor, Anonymous function
categories: JavaScript
---

### Function declaration 

{% highlight javascript %}
function name([param[, param[, ... param]]]) {
   statements
}
{% endhighlight %}

#### Example

{% highlight javascript %}
function sum(a, b)
{
    return a + b;
}
{% endhighlight %}

name - The function name

param - The name of the argument to be passed to the function. A function can have up to 255 arguments.

statements - The body of the function

### Function expression

{% highlight javascript %}
function [name]([param] [, param] [..., param]) {
   statements
}
{% endhighlight %}

#### Example 

{% highlight javascript %}
var sum = function(a, b) { return a + b; }
{% endhighlight %}


### Anonymous function

The name can be omitted in which case it becomes anonymous function.
Anonymous functions can help make code more concise when declaring a function that will only be used in one place. 

#### Example 

{% highlight javascript %}
var ar = [1,2,3];
var newAr = ar.map(function(e) { return e * 2});
console.log(newAr); //[2,4,6]
{% endhighlight %}

### Function constructor

Function objects can be created with new operator

{% highlight javascript %}
new Function (arg1, arg2, ... argN, functionBody)
{% endhighlight %}

#### Example

{% highlight javascript %}
var sum = new Function('a','b', 'return a + b;');
{% endhighlight %}

arg1, arg2, ... argN - zero or more names to be used by the function as argument names

functionBody - A string containing JavaScript statements forming the function body.

### References
- [Functions](https://developer.mozilla.org/en/JavaScript/Reference/Functions_and_function_scope)
- [Why do you need to invoke an anonymous function on the same line? ](http://stackoverflow.com/questions/1140089/how-does-an-anonymous-function-in-javascript-work)

 