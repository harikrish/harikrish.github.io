---
layout: post
title:  "JavaScript Array"
date:   2020-08-20 11:37:00 -0700
categories: [JavaScript]
---

An array is an ordered list of values that you refer to with a name and an index.
JavaScript does not have a explicity array data type. JavaScript provides
predefined Array object and methods to work with arrays.

{% highlight javascript %}
let arr1 = new Array(1, 2, 3, 4, 5);
let arr2 = ['a', 'b', 'c']; // Bracket sytax is called an "array literal"

let arr3 = new Array(10); //creates array with non zero length, but without any items.

let arr4 = Array.of(10); //creates a array with only one element. Array.of a static method in ES2015
{% endhighlight %}

### Iterating over arrays

{% highlight javascript %}
let myarr = [1, 2, 3, 4, 5];
for(let i = 0; i < myarr.length; i++) {
    console.log(myarr[i]); // 1, 2, 3, 4, 5
}

myarr.forEach(function(item) {
    console.log(item); // 1, 2, 3, 4, 5
});
{% endhighlight %}

### Array methods

- concat() - joins two or more arrays and returns a new array.
- join() - joins all elements of an array into a string.
- push() - adds one or more elements to the end of an array and returns the `length` of the array.
- pop() - removes the last element from the array and returns the element.
- shift() - removes the first element from the array and returns the element.
- unshift() - adds one or elements to the front of the array and returns the new `length` of the array.
- slice() - extracts a section of the array returns a new array.
- splice() - removes elements from an array and optionally replaces them. It returns the items that were removed from the array.
- reverse() - transposes the elements of the array.
- sort() - sorts the elements of the array in place.
- indexOf() - searches the array for the search element and returns the index of first match.
- lastIndexOf() - searches backward and works like indexOf()
- forEach() - executes a callback on every array item.
- map() - executes a callback on every item and returns a new array of the return value of the callback.
- filter() - executes a callback on every item and returns a new array containing the items for which callback returned `true`.
- every() - executes a callback on every item and returns true if callback returns `true` for every item.
- some() - executes a callback on every item and returns true if callback returns `true` for some item.
- reduce() - executes a callback on every item for the purpose of reducing the list of items down to single value.
- reduceRight() - works like reduce() but starts with the last element.

### References:
- [Indexed collections](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections)