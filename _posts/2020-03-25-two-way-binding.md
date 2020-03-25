---
layout: post
title:  "Two way binding"
date:   2020-03-25 06:35:48 -0700
categories: javascript
---

Two-way data-binding is a mechanism that synchronizes data in a bidirectional way.
Two-way binding is a pattern that connects a data model to the UI.

Two-way data binding in Angular really just boils down to property binding and event binding. 

{% highlight html %}
// code from https://blog.thoughtram.io/angular/2016/10/13/two-way-data-binding-in-angular-2.html
<input [value]="username" (input)="username = $event.target.value">

<p>Hello {{username}}!</p>

{% endhighlight %}

We’re binding the value of the username expression to the input’s value property (data goes into the component).
We also bind an expression to the element’s input event. This expression assigns the value of $event.target.value to the username model. 

References:
- https://www.bennadel.com/blog/3538-on-the-irrational-demonization-of-two-way-data-binding-in-angular.htm
- https://itnext.io/two-way-binding-in-react-a-concise-what-why-and-how-guide-22e76d4551d5
- https://www.wintellect.com/data-binding-pure-javascript/
- https://blog.thoughtram.io/angular/2016/10/13/two-way-data-binding-in-angular-2.html
- https://dev.to/phoinixi/two-way-data-binding-in-vanilla-js-poc-4e06