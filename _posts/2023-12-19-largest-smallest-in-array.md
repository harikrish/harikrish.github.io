---
layout: post
title:  "Find largest and smallest number in an array?"
date:   2023-12-19 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Assign first element of array to largest and smallest
- Iterate over the array
- If element is larger than largest, assign to largest
- If element is smaller than smallest, assign to smallest


{% highlight javascript %}
function findLargestSmallestInArray(arr) {
    let largest = arr[0];
    let smallest = arr[0];

    for(let i = 0; i< arr.length; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
        if (arr[i] < smallest) {
            smallest = arr[i];
        }
    }

    return [largest, smallest];
}

findLargestSmallestInArray([20,14,592,57,2,4,50,1]);
{% endhighlight %}



### References:
- [Find Smallest and Largest Element in an Array in Java](https://java2blog.com/java-program-to-find-smallest-and-largest-number-in-array/)