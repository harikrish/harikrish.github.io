---
layout: post
title:  "Implement Stack using JS"
date:   2024-01-02 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Stack has methods add, remove, peek, size, clear


{% highlight javascript %}
class Stack {
    constructor() {
        this.items = [];
    }

    add(element) {
        this.items.push(element);
    }

    remove() {
        if(this.items.length > 0) {
            return this.items.pop();
        }
    }

    peek() {
        return this.items[this.items.length - 1];
    }

    size() {
        return this.items.length;
    }

    clear() {
        this.items = [];
    }
}

let s = new Stack();
s.add(2);
s.add(3);
s.size();
s.items;
s.remove();
s.peek();
s.items;
s.clear();
s.items;
{% endhighlight %}



### References:
- [JavaScript Program to Implement a Stack](https://www.programiz.com/javascript/examples/stack)