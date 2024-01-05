---
layout: post
title:  "Implement Queue using JS"
date:   2024-01-05 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
Queue has following methods
- Enqueue - Add element to the end of queue
- Dequeue - Remove element from the front of queue
- isEmpty - Check if queue is empty
- isFull - Check if queue is full
- Peek - Get the value from front of queue without removing it

{% highlight javascript %}
class Queue {
    constructor() {
        this.items = {};
        this.headIndex = 0;
        this.tailIndex = 0;
    }

    enqueue(element) {
        this.items[this.tailIndex] = element;
        this.tailIndex++;
    }

    dequeue() {
        let el = this.items[this.headIndex];
        delete this.items[this.headIndex];
        if (this.isEmpty()) {
            this.headIndex = 0;
            this.tailIndex = 0;
        } else {
            this.headIndex++;
        }
        
        return el;
    }

    peek() {
        return this.items[this.headIndex];
    }

    isEmpty() {
        return (this.tailIndex - this.headIndex === 0);
    }

    clear() {
        this.items = {};
        this.headIndex = 0;
        this.tailIndex = 0;
    }
}

let q = new Queue();
q.enqueue(20);
q.enqueue(4);
q.items;
q.dequeue();
q.items;
q.clear();
q.items;

{% endhighlight %}



### References:
- [JavaScript Program to Implement a Queue](https://www.programiz.com/javascript/examples/queue)