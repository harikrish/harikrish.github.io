---
layout: post
title:  "Hoisting in JavaScript"
date:   2020-03-17 06:35:48 -0700
categories: JavaScript
---

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

### Variable hoisting
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

In EcmaScript2015(ES6), `let` and `const` are hoisted but not initialized.

{% highlight javascript %}
console.log(x); // Cannot access 'x' before initialization
let x = 10;
{% endhighlight %}

### Function hoisting

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

{% highlight javascript %}
var text = 'outside';

function print(){
    console.log(text);
    var text = 'inside';
};
print(); // Output: undefined, as only declaration was hoisted, no initialization happened.
{% endhighlight %}

#### References:
- [Understanding Hoisting in JavaScript](https://scotch.io/tutorials/understanding-hoisting-in-javascript)
- [Grammar and types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types)