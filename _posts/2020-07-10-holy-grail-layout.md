---
layout: post
title:  "Holy Grail CSS Layout"
date:   2020-07-10 13:04:00 -0700
categories: [CSS, HTML]
---

<p style="font-size: 0.9rem;font-style: italic;"><img style="display: block;" src="https://upload.wikimedia.org/wikipedia/commons/a/ad/HolyGrail.svg" alt="File:HolyGrail.svg"><a href="https://commons.wikimedia.org/w/index.php?curid=42413988">"File:HolyGrail.svg"</a><span> by <a href="https://commons.wikimedia.org/w/index.php?title=User:Davidlark&action=edit&redlink=1">David Lark</a></span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0?ref=ccsearch&atype=html" style="margin-right: 5px;">CC BY-SA 4.0</a><a href="https://creativecommons.org/licenses/by-sa/4.0?ref=ccsearch&atype=html" target="_blank" rel="noopener noreferrer" style="display: inline-block;white-space: none;margin-top: 2px;margin-left: 3px;height: 22px !important;"><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc_icon.svg" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-by_icon.svg" /><img style="height: inherit;margin-right: 3px;display: inline-block;" src="https://search.creativecommons.org/static/img/cc-sa_icon.svg" /></a></p>

Holy Grail is a layout pattern that’s very common on the web. 
It consists of a header, a main content area with fixed-width navigation on the left,
content in the middle and a fixed-width sidebar on the right and then a footer.

It is commonly desired and implemented, but for many years, 
the various ways in which it could be implemented with available technologies all had drawbacks. 
Because of this, finding an optimal implementation was likened to searching for the elusive Holy Grail.

Below example is taken from [In Search of the Holy Grail](https://alistapart.com/article/holygrail/)

{% highlight html %}
<div id="header"></div><div id="container">
  <div id="center" class="column"></div>
  <div id="left" class="column"></div>
  <div id="right" class="column"></div></div><div id="footer"></div>
{% endhighlight %}

{% highlight css %}

body {
  min-width: 550px;      /* 2x LC width + RC width */
}
#container {
  padding-left: 200px;   /* LC width */
  padding-right: 150px;  /* RC width */
}
#container .column {
  position: relative;
  float: left;
}
#center {
  width: 100%;
}
#left {
  width: 200px;          /* LC width */
  right: 200px;          /* LC width */
  margin-left: -100%;
}
#right {
  width: 150px;          /* RC width */
  margin-right: -150px;  /* RC width */
}
#footer {
  clear: both;
}
/*** IE6 Fix ***/
* html #left {
  left: 150px;           /* RC width */
}

{% endhighlight %}

### References:
- [In Search of the Holy Grail](https://alistapart.com/article/holygrail/)
- [Holy grail (web design)](https://en.wikipedia.org/wiki/Holy_grail_(web_design))
- [CSS Grid: Holy Grail Layout](https://alligator.io/css/css-grid-holy-grail-layout/)
- [THE HOLY GRAIL LAYOUT WITH 5 LINES OF CSS](https://css-tricks.com/books/fundamental-css-tactics/holy-grail-layout-5-lines-css/)