---
layout: post
title:  "What is AMD, CommonJS"
date:   2020-03-17 05:30:00 -0700
categories: JavaScript
---

### AMD (Asynchronous Module Definition) 
The AMD module format itself is a proposal for defining modules where both the module and dependencies can be asynchronously loaded. 

"define" method for facilitating module definition and a "require" method for handling dependency loading.

{% highlight javascript %}

define('myModule', 
    ['foo', 'bar'], 
    // module definition function
    // dependencies (foo and bar) are mapped to function parameters
    function ( foo, bar ) {
        // return a value that defines the module export
        // (i.e the functionality we want to expose for consumption)
    
        // create your module here
        var myModule = {
            doStuff:function(){
                console.log('Yay! Stuff');
            }
        }
 
        return myModule;
});

{% endhighlight %}

{% highlight javascript %}


require(['foo', 'bar'], function ( foo, bar ) {
        // rest of your code here
        foo.doSomething();
});


{% endhighlight %}

Module API supported by RequireJS is AMD. 
{% highlight javascript %}
//Calling define with a dependency array and a factory function
define(['dep1', 'dep2'], function (dep1, dep2) {

    //Define the module value by returning a value.
    return function () {};
});
{% endhighlight %}
- Register the factory function by calling define(), instead of immediately executing it.
- Pass dependencies as an array of string values.
- Only execute the factory function once all the dependencies have been loaded and executed.
- Pass the dependent modules as arguments to the factory function.

### CommonJS (CJS)

CJS module is a reusable piece of JavaScript which exports specific objects made available to any dependent code - there are typically no function wrappers around such modules.

{% highlight javascript %}

// package/lib is a dependency we require
var lib = require('package/lib');
 
// some behaviour for our module
function foo(){
    lib.log('hello world!');
}
 
// export (expose) foo to other modules
exports.foo = foo;

{% endhighlight %}

{% highlight javascript %}

// an application consuming 'foobar'
 
// access the module relative to the path
// where both usage and module files exist
// in the same directory
 
var foobar = require('./foobar').foobar,
    test   = new foobar();
 
test.bar(); // 'Hello bar'

{% endhighlight %}

### References
- [Writing Modular JavaScript With AMD, CommonJS & ES Harmony](https://addyosmani.com/writing-modular-js/)
- [MODULE PURPOSES](https://requirejs.org/docs/whyamd.html#purposes)