---
layout: post
title:  "Fid sum of natural numbers using recursion"
date:   2023-12-29 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Create program using recursion
- Call the function recursively until number is 1.


{% highlight javascript %}
function sum(num) {
    let val = 0;
    if (num > 0) {
        val = num + sum(num - 1);
    } else {
        val = num;
    }
    return val;
}

sum(6);
{% endhighlight %}



### References:
- [JavaScript Program to Find Sum of Natural Numbers Using Recursion](https://www.programiz.com/javascript/examples/number-sum-recursion)