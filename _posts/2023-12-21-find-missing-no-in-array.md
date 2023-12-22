---
layout: post
title:  "Find missing number in an array?"
date:   2023-12-21 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Create a set object having values within the range of initial
and final values of the provided array
- Then compare it with the provided array to retrieve the missing value


{% highlight javascript %}
function findMissingNumberInArray(arr) {
    const mySet = new Set();
    const firstEl = arr[0];
    const lastEl = arr[arr.length - 1];
    for(let i = firstEl; i <= lastEl; i++) {
        mySet.add(i);
    }
    for(let x = 0; x < arr.length; x++) {
        if(mySet.has(arr[x])) {
            mySet.delete(arr[x]);
        }
    }
    return Array.from(mySet);
}

findMissingNumberInArray([1,4,6,7,8,9]);
{% endhighlight %}



### References:
- [Find Missing Number in a given Array Using Python](https://djangocentral.com/find-missing-number-in-an-array-using-python/)
- [Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)