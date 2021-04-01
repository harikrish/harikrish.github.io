---
layout: post
title:  "Difference between DOMContentLoaded vs Load event in web page"
date:   2021-04-01 15:07:00 -0700
categories: [HTTP, Web]
---

The `DOMContentLoaded` event fires when the initial HTML document has been completely loaded
and parsed, without waiting for stylesheets, images, and subframes to finish loading.
`DOMContentLoaded` typically marks when both the DOM and CSSOM are ready.
If there is no parser blocking JavaScript then `DOMContentLoaded` event will fire
immediately after `domInteractive`.
When the browser processes an HTML-document and comes across a `<script>` tag, it needs to 
execute before continuing building the DOM. That's a precaution, as scripts may want to modify
DOM, and event `document.write` into it, so `DOMContentLoaded` has to wait.
Scripts with `async` attribute, don't block `DOMContentLoaded`.
Scripts that are generated dynamically with `document.createElement('script')` and then added to the 
webpage don't block `DOMContentLoaded` event.
External style sheeds don't affect DOM, so `DOMContentLoaded` does not wait for them.
But if we have script after a style, then the script must wait until the stylesheet loads.
The reason for this is that script may need style-dependent properties of elements.
So as `DOMContentLoaded` waits for scripts, it now waits for styles before them as well.

{% highlight javascript %}
window.addEventListener('DOMContentLoaded', (event) => {
    console.log('DOM fully loaded and parsed);
});
{% endhighlight %}

The `load` event is fired when the whole page has loaded, including all dependent resources such 
as stylesheets and images. 

{% highlight javascript %}
window.addEventListener('load', (event) => {
    console.log('page is fully loaded);
});
{% endhighlight %}

### References
- [Window:load event](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event)
- [Window:DOMContentLoaded event](https://developer.mozilla.org/en-US/docs/Web/API/Window/DOMContentLoaded_event)
- [Measuring the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp)
- [Page: DOMContentLoaded, load, beforeunload, unload](https://javascript.info/onload-ondomcontentloaded)