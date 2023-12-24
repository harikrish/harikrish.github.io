---
layout: post
title:  "Factorial of a number"
date:   2023-12-24 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Create program using recursion
- Until the value is not equal to zero, the recursive 
function will call itself


{% highlight javascript %}
function factorial(n) {
    if (n === 0) {
        return 1;
    }
    return n * factorial(n - 1);
}

factorial(5)
{% endhighlight %}



### References:
- [Program for factorial of a number](https://www.geeksforgeeks.org/program-for-factorial-of-a-number/)