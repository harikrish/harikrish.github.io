---
layout: post
title:  "How Do You Reverse a String?"
date:   2023-12-17 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Create a empty string `newString`
- Create a for loop, the starting point of the loop with be `str.length - 1`
which will be the last character of the string
- Continue for loop till `i` is greater than or equals `0`, decrement `i`
after each iteration


{% highlight javascript %}
function reverseString(str) {
    let newString = "";

   for(let i = str.length - 1 ; i >= 0; i--) {
       newString = newString + str[i];
   }

    return newString;
}

reverseString('hello');
{% endhighlight %}



### References:
- [64 Coding Interview Questions + Answers [2023 Prep Guide]](https://www.springboard.com/blog/software-engineering/coding-interview-questions/)
- [Three Ways to Reverse a String in JavaScript](https://www.freecodecamp.org/news/how-to-reverse-a-string-in-javascript-in-3-different-ways-75e4763c68cb/)