---
layout: post
title:  "Bubble Sort"
date:   2020-03-20 06:35:48 -0700
categories: [Algorithm, JavaScript, Interview, Coding]
---

The bubble sort makes multiple passes through a list. It compares adjacent items and exchanges those that are out of order. Each pass through the list places the next largest value in its proper place. In essence, each item “bubbles” up to the location where it belongs.

If there are n items in the list, then there are n−1 pairs of items that need to be compared on the first pass. It is important to note that once the largest value in the list is part of a pair, it will continually be moved along until the pass is complete.

At the start of the second pass, the largest value is now in place. There are n−1 items left to sort, meaning that there will be n−2 pairs. Since each pass places the next largest value in place, the total number of passes necessary will be n−1. After completing the n−1 passes, the smallest item must be in the correct position with no further processing required. 

{% highlight javascript %}

 function countSwaps(a) {
    let numSwaps = 0;
    for (let p = a.length ; p > 0 ; p--) {
        for (let x = 0; x < p - 1 ; x++) {
            if (a[x] > a[x + 1]) {
                let swap = a[x];
                a[x] = a[x + 1];
                a[x + 1] = swap;
                numSwaps++;
            }
        }
    }
    console.log(`Array is sorted in ${numSwaps} swaps.`);
    console.log(`First Element: ${a[0]}`);
    console.log(`Last Element: ${a[a.length -1]}`);
 }

{% endhighlight %}

References:
- [The Bubble Sort](https://runestone.academy/runestone/books/published/pythonds/SortSearch/TheBubbleSort.html)