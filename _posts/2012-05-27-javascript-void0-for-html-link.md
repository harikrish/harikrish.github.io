---
layout: post
title: javascript void(0) for HTML link
categories: [JavaScript, HTML]
---

To create a HTML link which does nothing when user clicks it,  use  like below


<A HREF="javascript:void(0)">Click here to do nothing</A>

When the user clicks the link, 
void(0) evaluates to undefined, which has no effect in JavaScript.

References -


[https://developer.mozilla.org/en/JavaScript/Guide/Expressions_and_Operators#void](https://developer.mozilla.org/en/JavaScript/Guide/Expressions_and_Operators#void)

Here is a stackoverflow.com link, which answers why  
void(0)  is better than using 
#  for this requirement


[http://stackoverflow.com/questions/134845/href-for-javascript-links-or-javascriptvoid0](http://stackoverflow.com/questions/134845/href-for-javascript-links-or-javascriptvoid0)