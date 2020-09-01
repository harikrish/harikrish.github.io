---
layout: post
title: JavaScript data types, variables, variable scope, literals, hoisting
categories: JavaScript
---

#### Data types

JavaScript has six primitive data types,

`undefined` - A variable that has not been assigned a value is of type `undefined`.
	
`null` - A special keyword denoting a null value.

Boolean - A logical entity that consists of either a `true` or `false` value.

Number - A set of numerical digits that represent a number.

String - A set of zero or more characters.

Symbol - It is a new feature in ECMAScript 2015 (ES6).
Symbols are tokens that serve as unique IDs.

#### Variables

You can use variables as symbolic names for values in application. The names of variables, is called identifiers. Variables can be declared with keyword `var`.

#### Variable scope

When you declare variables outside of function , its called global variable. When you declare within a function, its called local variable. JavaScript does not have block statement scope.

#### Hoisting

You can refer to variable declared later without getting exception. This concept is called "Hoisting", variables in JavaScript are in a sense "hoisted" or lifted to the top of the function.

#### Constants

You can create read-only, named constant with `const` keyword.  A constant cannot change value through assignment.

#### Literals

These are fixed values, not variables, that you literally provide in you script.

- Array Literals

{% highlight javascript %}
var coffees = ["French Roast","Colombian","Kona"];
{% endhighlight %}

- Boolean Literals

The boolean type has two literal values `true`, `false`.

- Object Literals

An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces.

{% highlight javascript %}

var solarSystem = { 
    planets: ['mercury', 'venus', 'neptune', 'mars', 'earth', 'jupiter', 'saturn', 'uranus']
};

{% endhighlight %}

- String literals

A string literal is zero or more characters enclosed in double or single quotation marks.

{% highlight javascript %}
'foo'
"baz"
{% endhighlight %}

- Template literals

EcmaScript2015(ES6) introduced Template literals. They are text enclosed in back ticks
instead of double or single quotes.

{% highlight javascript %}
`Hello world!`
{% endhighlight %}

#### References
- [Data and Structure types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
- [Symbols in ECMAScript 6](https://2ality.com/2014/12/es6-symbols.html)
- [Grammar and types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types)
- [Data types](https://javascript.info/types)