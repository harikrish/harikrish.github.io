---
layout: post
title: JavaScript binding, function apply, function call
date:   2012-12-28 12:47:00 -0700
categories: JavaScript
---

In JavaScript, binding is always explicit, and can be easily lost, so a method using "this" will not refer to the proper object in all situations,  unless you force it to.
JavaScript provides two options to do explicit binding "apply" and "call".

### Apply
Every JavaScript function is equipped with "apply" method that allows you to call the function with specific binding. I takes two arguments, the binding object and an array of arguments to be passed to the function.
{% highlight javascript %}
fun.apply(thisArg[, argsArray])
{% endhighlight %}

### Call
"Call" method is similar to "apply", but it takes the arguments themselves not an array.
{% highlight javascript %}
fun.call(thisArg[, arg1[, arg2[, ...]]])
{% endhighlight %}

References
- http://www.alistapart.com/articles/getoutbindingsituations
- https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Function/apply
- https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Function/call
- http://stackoverflow.com/questions/962033/what-underlies-this-javascript-idiom-var-self-this