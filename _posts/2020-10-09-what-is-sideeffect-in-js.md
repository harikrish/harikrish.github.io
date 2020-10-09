---
layout: post
title:  "What is a side effect in JavaScript?"
date:   2020-10-09 10:34:00 -0700
categories: [JavaScript]
---

A side effect is any application state change that 
is observable outside the called function other than its
return value. For example modifying any external variable
like global variable, logging to console, writing to file,
writing to network, calling other functions with side effects.

{% highlight javascript %}
function printSomething(foo) {
    console.log(foo);
}
// printing to console make this function to have a side effect.
{% endhighlight %}

Side effects are mostly avoided in functional programming, which
makes the program easier to understand and to test.

### References:
- [Master the JavaScript Interview: What is Functional Programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)
- [3 common approaches to side-effects in Redux apps](https://goshakkk.name/redux-side-effect-approaches/)
- [Redux side effects and me
](https://medium.com/magnetis-backstage/redux-side-effects-and-me-89c104a4b149)
- [Preventing Side Effects in JavaScript](https://davidwalsh.name/preventing-sideeffects-javascript)
- [HOW TO DEAL WITH DIRTY SIDE EFFECTS IN YOUR PURE FUNCTIONAL JAVASCRIPT](https://jrsinclair.com/articles/2018/how-to-deal-with-dirty-side-effects-in-your-pure-functional-javascript/)
- [Dealing with side effects and pure functions in javascript](https://dev.to/vonheikemen/dealing-with-side-effects-and-pure-functions-in-javascript-16mg)