---
layout: post
title:  "Linked list using JavaScript"
date:   2024-02-19 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

A linked list is a linear data structure that includes a series of connected nodes. Here each
node stores the data and the address of the next node.

Linked list methods:
- size() - Returns the number of nodes present in the linked list.
- clear() - Empties out the list.
- getLast() - Returns the last node of the linked list.
- getFirst() - Returns the first node of the linked list.

{% highlight javascript %}
class ListNode {
    constructor(data) {
        this.data = data;
        this.next = null;
    }
}

class LinkedList {
    constructor(head = null) {
        this.head = head;
    }

    size() {
        let count = 0;
        let node = this.head;

        while (node) {
            count++;
            node = node.next;
        }
        return count;
    }

    clear() {
        this.head = null;
    }

    getLast() {
        let lastNode = this.head;

        if(lastNode) {
            while (lastNode.next) {
                lastNode = lastNode.next;
            }
        }
        return lastNode;
    }

    getFirst() {
        return this.head;
    }
}

let node1 = new ListNode(2);
let node2 = new ListNode(5);
node1.next = node2;

let list = new LinkedList(node1);


list.head.data;
list.head.next.data;
list.size();

list.getFirst();

list.getLast();

{% endhighlight %}

### References:
- [How to Implement a Linked List in JavaScript](https://www.freecodecamp.org/news/implementing-a-linked-list-in-javascript/)
- [Linked list Data Structure](https://www.programiz.com/dsa/linked-list)