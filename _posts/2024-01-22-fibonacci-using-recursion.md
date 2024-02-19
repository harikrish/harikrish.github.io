---
layout: post
title:  "Print fibonacci sequence using recursion"
date:   2024-01-22 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
The fibonnaci sequence is the integer sequence where the first
two terms are `0` and `1`. After that, the next term is defined as 
the sum of the previous two terms.
Hence the nth term is sum of `n-1` term and `n-2` term.

{% highlight javascript %}

function fibonnaci(num) {
    if (num < 2) {
        return num;
    } else {
        return fibonnaci(num - 1) + fibonnaci(num - 2);
    }
}

let arr = [];
for(let i = 0; i < 10; i++) {
    arr.push(fibonnaci(i));
}

console.log(arr);

{% endhighlight %}


### References:
- [JavaScript Program to Display Fibonacci Sequence Using Recursion](https://www.programiz.com/javascript/examples/fibonacci-recursion)