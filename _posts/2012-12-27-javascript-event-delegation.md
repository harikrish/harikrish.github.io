---
layout: post
title: JavaScript event delegation
categories: JavaScript
---

JavaScript event delegation is a simple technique by which you add a single event handler to a parent element in order to avoid having to add event handlers to multiple child elements.

### Event capturing

Netscape defined an approach called event capturing, where events occur on the highest object in the DOM tree and then work down to the deepest element affected by the event.

### Event bubbling

IE defined event bubbling. The deepest element affected by the event should receive the event first , then its parent, etc., until the document object finally receives the event.

W3C DOM level 2 events specification defines both event bubbling and capturing. First the document receives the event, then the capturing phase commences to the most specific element affected by the event. Once the event is handled by the element, it bubbles back up to the document.

### Advantages
- Less event handlers to setup and reside in memory.
- No need to re-attach handlers after a DOM update.

### References:

- [http://www.nczonline.net/blog/2009/06/30/event-delegation-in-javascript/](http://www.nczonline.net/blog/2009/06/30/event-delegation-in-javascript/)
- [http://www.sitepoint.com/javascript-event-delegation-is-easier-than-you-think/](http://www.sitepoint.com/javascript-event-delegation-is-easier-than-you-think/)