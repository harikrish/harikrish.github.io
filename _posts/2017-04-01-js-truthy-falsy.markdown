---
layout: post
title:  "Truth and Falsy in JavaScript"
date:   2017-04-01 10:35:40 -0700
categories: JavaScript
---

In JavaScript, a truthy value is a value that is considered  true when
evaluated in a Boolean context.

A falsy value is a value that translates to false when evaluated in a
Boolean context.

All values are truthy unless they are defined as falsy
(i.e., except for false, 0, "", null, undefined, and NaN).

The falsy values null and undefined are not equivalent to anything
except themselves.

The falsy value NaN is not equivalent to anything — including NaN!

Use strict equal (===) and strict not equal (!==) in situations
where truthy or falsy values could lead to logic errors.


- References

https://www.sitepoint.com/javascript-truthy-falsy/

https://developer.mozilla.org/en-US/docs/Glossary/Truthy

https://developer.mozilla.org/en-US/docs/Glossary/Falsy
