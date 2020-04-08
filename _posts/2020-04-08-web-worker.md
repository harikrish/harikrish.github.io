---
layout: post
title:  "Web Workers"
date:   2020-04-08 06:56:00 -0700
categories: javascript
---

The Web Workers specification defines an API for spawning background scripts in your web application. Web Workers allow you to do things like fire up long-running scripts to handle computationally intensive tasks, but without blocking the UI or other scripts to handle user interactions. 

{% highlight javascript %}
// Code from https://www.html5rocks.com/en/tutorials/workers/basics/

var worker = new Worker('task.js');
worker.postMessage(); // Start the worker.

{% endhighlight %}

Communication between a work and its parent page is done using an event model and the postMessage() method.

{% highlight javascript %}
// Code from https://www.html5rocks.com/en/tutorials/workers/basics/

// Main script
var worker = new Worker('doWork.js');

worker.addEventListener('message', function(e) {
  console.log('Worker said: ', e.data);
}, false);

worker.postMessage('Hello World'); // Send data to our worker.

// Worker script
self.addEventListener('message', function(e) {
  self.postMessage(e.data);
}, false);
{% endhighlight %}

There are two ways to stop a worker: by calling worker.terminate() from the main page or by calling self.close() inside of the worker itself.

References:
- https://www.html5rocks.com/en/tutorials/workers/basics/
- https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API