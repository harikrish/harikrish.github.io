---
layout: post
title: Referencing variables in setTimeout function - Javascript Closures
categories: JavaScript
---

Requirement

- Reference For loop variable i  in setTimeout function


Wrong way

{% highlight javascript %}
for(var i = 1 ; i <= 10; i++) {
    console.log('i in for :: ' + i);
    setTimeout(function() {
        console.log(' i in timeout :: ' + i);
    }, 2000);
}
{% endhighlight %}

Ouput
{% highlight javascript %}
i in for :: 1
i in for :: 2
i in for :: 3
i in for :: 4
i in for :: 5
i in for :: 6
i in for :: 7
i in for :: 8
i in for :: 9
i in for :: 10
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
i in timeout :: 11
{% endhighlight %}

Right way using Closures

{% highlight javascript %}
for(var i = 1 ; i <= 10; i++) {
    console.log('i in for :: ' + i);
    setTimeout(function(j) {
        return function() {
        console.log(' j in timeout :: ' + j);
    }
    }(i), 2000);
}
{% endhighlight %}

Ouput

{% highlight javascript %}
i in for :: 1
i in for :: 2
i in for :: 3
i in for :: 4
i in for :: 5
i in for :: 6
i in for :: 7
i in for :: 8
i in for :: 9
i in for :: 10
j in timeout :: 1
j in timeout :: 2
j in timeout :: 3
j in timeout :: 4
j in timeout :: 5
j in timeout :: 6
j in timeout :: 7
j in timeout :: 8
j in timeout :: 9
j in timeout :: 10
{% endhighlight %}


### References:
- [http://jibbering.com/faq/notes/closures/](http://jibbering.com/faq/notes/closures/)
- [https://developer.mozilla.org/en/JavaScript/Guide/Closures](https://developer.mozilla.org/en/JavaScript/Guide/Closures)