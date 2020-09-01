---
layout: post
title: javascript undefined, null, undefined property, 0, false, '', ==, ===, typeof
categories: [JavaScript]
---

== Equals>If the two operands are not of the same type, JavaScript converts the operands then applies strict comparison.

=== Strict equal

>Returns true if the operands are strictly equal  with no type conversion.

typeof

>The 
typeof operator returns a string indicating the type of the unevaluated operand.

typeof undefined === 'undefined'

undefined

>A variable that has not been assigned a value is of type undefined.

false

>Examples of expressions that can be converted to false are those that evaluate to null, 0, the empty string (""), or undefined.

null

>null is an object. It's type is null. Null and Undefined types are 
== (but not 
===)

Undeclared variable

>*/* var z*/

	
*z.x  // throws a ReferenceError

Check for undefined variable

*var x;

	
*if (x === undefined) {

	
*   // these statements execute

	
*}

	
*else {

	
*   // these statements do not execute

	
*}
check for undeclared variable

*// x has not been defined before

	
*if (typeof x === 'undefined') { // evaluates to true without errors

	
*   // these statements execute

	
*}

	
*

	
*if(x === undefined){ // throws a ReferenceError

	
*

	
*}
check for object property

*var myobj = {'a':'a'};

	
*myobj.hasOwnProperty('a') // true

	
*var myobj2 = Object.create(myobj);

	
*myobj2.hasOwnProperty('a') //false

	
*'a' in myobj2 // true
check for null

*var c = null

	
*if (c === null) { // true

	
*}
References


[http://saladwithsteve.com/2008/02/javascript-undefined-vs-null.html](http://saladwithsteve.com/2008/02/javascript-undefined-vs-null.html)


[http://constc.blogspot.com/2008/07/undeclared-undefined-null-in-javascript.html](http://constc.blogspot.com/2008/07/undeclared-undefined-null-in-javascript.html)


[http://www.mapbender.org/JavaScript_pitfalls:_null,_false,_undefined,_NaN](http://www.mapbender.org/JavaScript_pitfalls:_null,_false,_undefined,_NaN)


[https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/undefined](https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/undefined)


[https://developer.mozilla.org/en/JavaScript/Reference/Operators/Comparison_Operators](https://developer.mozilla.org/en/JavaScript/Reference/Operators/Comparison_Operators)


[https://developer.mozilla.org/en/JavaScript/Reference/Operators/typeof](https://developer.mozilla.org/en/JavaScript/Reference/Operators/typeof)


[http://www.nczonline.net/blog/2010/07/27/determining-if-an-object-property-exists/](http://www.nczonline.net/blog/2010/07/27/determining-if-an-object-property-exists/)