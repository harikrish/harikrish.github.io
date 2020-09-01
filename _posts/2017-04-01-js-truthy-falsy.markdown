---
layout: post
title:  "Truth and Falsy in JavaScript"
date:   2017-04-01 10:35:40 -0700
categories: JavaScript
---

Javascript auto converts any value used in Boolean context (example an `if` condition) 
to either `true` or `false`. This way of implicitly converting a type is 
called as Implicit Type Coercion.

In JavaScript, a truthy value is a value that is considered  `true` when
evaluated in a Boolean context.

A falsy value is a value that translates to `false` when evaluated in a
Boolean context.

The following values are treated as `false`.
- `false`
- `0` (the number zero)
- `""` or `''` (an empty string)
- `null`
- `undefined`
- `NaN` (the result of failed mathematical operations)

All values are truthy unless they are defined as falsy
(i.e., except for `false`, `0`, `""`, `null`, `undefined`, and `NaN`).

The falsy values `null` and `undefined` are not equivalent to anything
except themselves.

The falsy value `NaN` is not equivalent to anything — including `NaN`!

Use strict equal (`===`) and strict not equal (`!==`) in situations
where truthy or falsy values could lead to logic errors.

We can  test for several types of invalid data by simply passing a 
variable into an if expression. 
{% highlight javascript %}

if (value) {
  // value is truthy
}
else {
  // value is falsy
  // it could be false, 0, '', null, undefined or NaN
}
{% endhighlight %}


### References
- [Truthy and Falsy: When All is Not Equal in JavaScript](https://www.sitepoint.com/javascript-truthy-falsy/)
- [Truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)
- [Falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)
- [JavaScript quirk 1: implicit conversion of values](https://2ality.com/2013/04/quirk-implicit-conversion.html)
- [Type Conversions](https://javascript.info/type-conversions)