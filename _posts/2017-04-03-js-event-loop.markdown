---
layout: post
title:  "What is JavaScript Event Loop ?"
date:   2017-04-03 05:55:35 -0700
categories: javascript
---

The event loop is in the heart of Node.js / Javascript -
it is responsible for scheduling asynchronous operations.

A very interesting property of the event loop model is that JavaScript,
unlike a lot of other languages, never blocks. Handling I/O is typically
performed via events and callbacks, so when the application is waiting
for an IndexedDB query to return or an XHR request to return,
it can still process other things like user input.

- References

http://altitudelabs.com/blog/what-is-the-javascript-event-loop/

http://2014.jsconf.eu/speakers/philip-roberts-what-the-heck-is-the-event-loop-anyway.html

https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop

https://blog.risingstack.com/node-hero-async-programming-in-node-js/
