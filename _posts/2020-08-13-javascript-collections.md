---
layout: post
title:  "JavaScript Collections"
date:   2020-08-13 13:31:00 -0700
categories: [JavaScript, ES6]
---

ECMAScript2015(ES6) introduced four new collections `Map`, `Set`, `WeakMap` and `WeakSet`.

### Map
A `Map` object is a simple key/value map and can iterate its elements 
in insertion order.

{% highlight javascript %}
let barMap = new Map();
barMap.set('one', 1);
barMap.set('two', 2);
barMap.set('three', 3);

for (let [key, value] of barMap) {
    console.log(key + ' = ' + value); // one = 1, two = 2, three = 3
}

barMap.forEach(function(value, key) {
    console.log(key + ' = ' + value); // one = 1, two = 2, three = 3
});
{% endhighlight %}

### Set
A `Set` object is a collection of values. A value in a set may only
occur once. You can iterate its elements in insertion order.

{% highlight javascript %}
let bazSet = new Set();
bazSet.add('a');
bazSet.add('b');
bazSet.add('c');

for (let value of bazSet) {
    console.log(value); // a, b, c
}
{% endhighlight %}

### WeakMap
A `WeakMap` is a collection of key/value pairs in which the keys are 
weakly referenced. The keys must be objects. They allow for objects
which are no longer needed to be cleared from memory.
There is no method to obtain a list of the keys.

{% highlight javascript %}
const foowm = new WeakMap();
const key1 = {};
foowm.set(key1, "value1");
foowm.get(key1); // "value1"
{% endhighlight %}

### WeakSet
A `WeakSet` is a collection of objects. References to objects are held weakly.
If no other references to an object stored in the `WeakSet` exist , those objects
can be garbage collected.

{% highlight javascript %}
const barws = new WeakSet();
const value1 = {};
barws.add(value1);
{% endhighlight %}

### References
- [ES6 Collections: Using Map, Set, WeakMap, WeakSet](https://www.sitepoint.com/es6-collections-map-set-weakmap-weakset/)
- [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
- [Keyed Collections](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Keyed_collections)
- [Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
- [WeakMap](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)
- [WeakSet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakSet)