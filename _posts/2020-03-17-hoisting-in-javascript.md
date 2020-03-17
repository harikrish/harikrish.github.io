---
layout: post
title:  "Hoisting in JavaScript"
date:   2020-03-17 06:35:48 -0700
categories: javascript
---

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

{% highlight javascript %}

console.log(hoist); // Output: undefined

var hoist = 'The variable has been hoisted.';

{% endhighlight %}

{% highlight javascript %}

function hoist() {
  console.log(message); // Output: undefined
  var message='Hoisting is all the rage!'
}

hoist();

{% endhighlight %}

{% highlight javascript %}

function hoist() {
  a = 20;
  var b = 100;
}

hoist();

console.log(a); 
/* 
Accessible as a global variable outside hoist() function
Output: 20
*/

console.log(b); 
/*
Since it was declared, it is confined to the hoist() function scope.
We can't print it out outside the confines of the hoist() function.
Output: ReferenceError: b is not defined
*/

{% endhighlight %}

This means that, all undeclared variables are global variables.

{% highlight javascript %}

hoisted(); // Output: "This function has been hoisted."

function hoisted() {
  console.log('This function has been hoisted.');
};

{% endhighlight %}

Function expressions, however are not hoisted.

{% highlight javascript %}

expression(); //Output: "TypeError: expression is not a function

var expression = function() {
  console.log('Will this work?');
};

{% endhighlight %}

References:
- https://scotch.io/tutorials/understanding-hoisting-in-javascript
