---
layout: post
title:  "Document Object Model (DOM)"
date:   2020-04-04 14:30:00 -0700
categories: javascript
---

The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web. 

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

In the beginning, JavaScript and the DOM were tightly intertwined, but eventually, they evolved into separate entities. The page content is stored in the DOM and may be accessed and manipulated via JavaScript.

{% highlight javascript %}

const paragraphs = document.getElementsByTagName("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
alert(paragraphs[0].nodeName);

{% endhighlight %}

References:
- https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction