---
layout: post
title:  "JavaScript async and defer"
date:   2021-02-18 17:27:00 -0700
categories: [HTTP, Web, JavaScript]
---

The defer and async attributes were introduced to give developers
a way to tell the browser which scripts to handle asynchronously.
Both of these attributes tell the browser that it may go on parsing the
HTML while loading the script in background, and then execute the 
script after it loads. This way, script downloads don't block 
DOM construction and page rendering. So the user can see the page
before all scripts have finished loading.

The difference between `defer` and `async` is which momemt they 
start executing the scripts.
`defer` execution starts after parsing is completely finished,
but before the `DOMContentLoaded` event. It guarantees scripts
will be executed in the order they appear in the HTML and will 
not block the parser.
`async` scripts execute at the first opportunity after they finish
downloading and before the windows `load` event. This means it's
possible that async scripts are not executed in the order in which
they appear in the HTML. It also means they can interrupt DOM building.
`async` scripts load at a low priorty. They often load after all other
scripts, without blocking DOM building. 


### References
- [Building the DOM faster: speculative parsing, async, defer and preload](https://hacks.mozilla.org/2017/09/building-the-dom-faster-speculative-parsing-async-defer-and-preload/)
- [Scripts: async, defer](https://javascript.info/script-async-defer)
- [Async vs Defer - Which Script Attribute is More Efficient When Loading JavaScript?](https://curiosum.dev/blog/seo-speed-script-tags-async-vs-defer)