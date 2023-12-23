---
layout: post
title:  "Find if string is a palindrome?"
date:   2023-12-23 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Loop through the characters in the string
- Check if the first letter match the last letter
- Check second letter match the second to last letter


{% highlight javascript %}
function palindrome(str) {
    for(let i = 0; str.length - i > i; i++) {
        if (str[i] !== str[str.length - 1 - i]) {
            return false;
        }
    }
    return true;
}

palindrome('madam')
{% endhighlight %}



### References:
- [Algorithm: Palindrome](https://medium.com/@stevenpaulino1/algorithm-palindrome-6d0763c2f47c)