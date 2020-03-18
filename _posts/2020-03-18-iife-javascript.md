---
layout: post
title:  "What is Immediately-Invoked Function Expression (IIFE) ?"
date:   2020-03-17 06:35:48 -0700
categories: javascript
---

An IIFE or Immediately Invoked Function Expression is a function that is gonna get invoked or executed after its creation or declaration. The syntax for creating IIFE is that we wrap the function (){} inside a parentheses () or the Grouping Operator to treat the function as an expression and after that we invoke it with another parentheses (). So an IIFE looks like this 

{% highlight javascript %}

(function(){})().

{% endhighlight %}

An Immediately-Invoked Function Expression can be used to “lock in” values and effectively save state.

{% highlight javascript %}

  // This doesn't work like you might think, because the value of `i` never
  // gets locked in. Instead, every link, when clicked (well after the loop
  // has finished executing), alerts the total number of elements, because
  // that's what the value of `i` actually is at that point.

  var elems = document.getElementsByTagName( 'a' );

  for ( var i = 0; i < elems.length; i++ ) {

    elems[ i ].addEventListener( 'click', function(e){
      e.preventDefault();
      alert( 'I am link #' + i );
    }, 'false' );

  }

  // This works, because inside the IIFE, the value of `i` is locked in as
  // `lockedInIndex`. After the loop has finished executing, even though the
  // value of `i` is the total number of elements, inside the IIFE the value
  // of `lockedInIndex` is whatever the value passed into it (`i`) was when
  // the function expression was invoked, so when a link is clicked, the
  // correct value is alerted.

  var elems = document.getElementsByTagName( 'a' );

  for ( var i = 0; i < elems.length; i++ ) {

    (function( lockedInIndex ){

      elems[ i ].addEventListener( 'click', function(e){
        e.preventDefault();
        alert( 'I am link #' + lockedInIndex );
      }, 'false' );

    })( i );

  }

{% endhighlight %}

References:
- http://benalman.com/news/2010/11/immediately-invoked-function-expression/
- https://dev.to/macmacky/70-javascript-interview-questions-5gfi#26-what-is-an-iife-what-is-the-use-of-it