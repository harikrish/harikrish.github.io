---
layout: post
title:  "What is Promise Chaining?"
date:   2020-03-17 05:30:00 -0700
categories: JavaScript
---

A common need is to execute two or more asynchronous operations back to back, where each subsequent operation starts when the previous operation succeeds, with the result from the previous step. We accomplish this by creating a promise chain.

In the old days, doing several asynchronous operations in a row would lead to the classic callback pyramid of doom:

{% highlight javascript %}

doSomething(function(result) {
  doSomethingElse(result, function(newResult) {
    doThirdThing(newResult, function(finalResult) {
      console.log('Got the final result: ' + finalResult);
    }, failureCallback);
  }, failureCallback);
}, failureCallback);

{% endhighlight %}

With modern functions, we attach our callbacks to the returned promises instead, forming a promise chain:

{% highlight javascript %}

doSomething()
.then(function(result) {
  return doSomethingElse(result);
})
.then(function(newResult) {
  return doThirdThing(newResult);
})
.then(function(finalResult) {
  console.log('Got the final result: ' + finalResult);
})
.catch(failureCallback);

{% endhighlight %}

Reference:
- [Using Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
- [Promises chaining](https://javascript.info/promise-chaining)
