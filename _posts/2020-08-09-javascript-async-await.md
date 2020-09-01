---
layout: post
title:  "JavaScript Async and Await"
date:   2020-08-09 11:06:00 -0700
categories: [JavaScript, ES8]
---

`async` functions and `await` are part of ECMAScript 2017(ES8).
These features basically act as syntactic sugar on top of promises.
They make asynchronous code look like synchronous code.
They make code much simpler and easier to understand.

### async functions

`async` functions returned values are guaranteed to be converted 
into promises.

{% highlight javascript %}

async function myFunc() {
    return "Hello World!";
}

myFunc().then((value) => {
    console.log(value); // Hello World!
})

{% endhighlight %}

### await keyword

`await` works only inside `async` functions. `await` keyword put in
front of any async promise based function causes the line to pause
until the promise fulfills.

{% highlight javascript %}
async function foo() {
    return icecream = await Promise.resolve("Vanilla Cone!");
}

foo().then((value) => {
    console.log(value); // Vanilla Cone!
});
{% endhighlight %}

#### References:
- [Making asynchronous programming easier with async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)
- [Async/await](https://javascript.info/async-await)