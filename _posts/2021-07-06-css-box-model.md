---
layout: post
title:  "CSS Box Model"
date:   2021-07-06 16:14:00 -0700
categories: [CSS, Web]
---

The CSS box model defines how the different parts of a box - 
margin, border, padding, and content - work together to 
create a box that can be seen on the page.

## Parts of a box
- Content box - The area where content is displayed, which
can be sized using properties like width and height.
-  Padding box - The padding sits around the content as
white space, its size is controlled using padding and 
related properties.
- Border box - The border box wraps the content and any padding.
Its sizing and style can be controlled using border and
related properties.
- Margin box - The margin is the outermost layer, wrapping
the content, padding and border as whitespace between this
box and other elements. Its size can be controlled using 
margin and related properties.

## Standard CSS box model
In the standard box model, if a box is given width and height
attribute, this defines the width and height of the content box.

## Alternative CSS box model
Using this model, any width is the width of the visible box
on the page, therefore the content area width is that the
width minux the width for the padding and border.

### References:
- [Introduction to the CSS basic box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
- [The box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
- [The CSS Box Model](https://css-tricks.com/the-css-box-model/)
