---
layout: post
title:  "What is JavaScript Event Loop ?"
date:   2017-04-03 05:55:35 -0700
categories: JavaScript
---

JavaScript code runs single threaded. 
Javascript has a concurrency model based on an event loop.
The event loop is in the heart of Node.js / Javascript -
it is responsible for scheduling asynchronous operations.
A very interesting property of the event loop model is that JavaScript,
unlike a lot of other languages, never blocks. Handling I/O is typically
performed via events and callbacks, so when the application is waiting
for an IndexedDB query to return or an XHR request to return,
it can still process other things like user input.

Two main parts of the event loop are the call stack and the message queue.

The call stack is a LIFO queue (Last In, First Out).

The Message Queue is also where user-initiated events like click or keyboard events, or fetch responses are queued before your code has the opportunity to react to them. Or also DOM events like onLoad.

Event Loop is a process that constantly checks whether the call stack is empty, and whenever it’s empty, it checks if the event queue has any functions waiting to be invoked. If it does, then the first function in the queue gets invoked and moved over into the call stack. If the event queue is empty, then this monitoring process just keeps on running indefinitely. 

### Async callbacks

An asynchronous callback function is just like any other function you’re used to writing in JavaScript, with the added caveat that it doesn’t get executed till later.

{% highlight javascript %}

(function() {

  console.log('this is the start');

  setTimeout(function cb() {
    console.log('Callback 1: this is a msg from call back');
  }); // has a default time value of 0

  console.log('this is just a message');

  setTimeout(function cb1() {
    console.log('Callback 2: this is a msg from call back');
  }, 0);

  console.log('this is the end');

})();

// "this is the start"
// "this is just a message"
// "this is the end"
// "Callback 1: this is a msg from call back"
// "Callback 2: this is a msg from call back"

{% endhighlight %}

The use case of 
{% highlight javascript %}
setTimeout(() => {}), 0)
{% endhighlight %}
 is to call a function, but execute it once every other function in the code has executed.

### References

- [What is the JavaScript event loop? ](http://altitudelabs.com/blog/what-is-the-javascript-event-loop/)
- [The JavaScript Event Loop](https://flaviocopes.com/javascript-event-loop/)
- [The JavaScript Event Loop: Explained](https://blog.carbonfive.com/2013/10/27/the-javascript-event-loop-explained/)
- [Philip Roberts: What the heck is the event loop anyway?](http://2014.jsconf.eu/speakers/philip-roberts-what-the-heck-is-the-event-loop-anyway.html)
- [Concurrency model and the event loop
](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
- [Understanding Async Programming in Node.js](https://blog.risingstack.com/node-hero-async-programming-in-node-js/)
- [Introducing asynchronous JavaScript
](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing)
