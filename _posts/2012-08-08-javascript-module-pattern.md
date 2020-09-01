---
layout: post
title: Javascript Module Pattern
categories: JavaScript
---

Module Pattern - It stays out of the global namespace, provides publicly addressable API methods, and supports protected or “private” data and methods along the way.

{% highlight javascript %}

var myFunc = (function() {
    var privateProperty = 10;

    return {
        print: function() {
            console.log(privateProperty);
        },
        assign: function(a) {
            privateProperty = a;
        }
    }
})();

myFunc.print(); //10
myFunc.assign(100);
myFunc.print(); //100

{% endhighlight %}

The private variables can only be accessed from within the anonymous function itself or
from within a member of the `return`ed object. This is through the power of closuers.

### References

- [A JavaScript Module Pattern](http://www.yuiblog.com/blog/2007/06/12/module-pattern/)
- [Emulating private methods with closures
](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)