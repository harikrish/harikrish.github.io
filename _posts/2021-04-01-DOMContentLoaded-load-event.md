---
layout: post
title:  "Different between DOMContentLoaded vs Load event in web page"
date:   2021-04-01 15:07:00 -0700
categories: [HTTP, Web]
---

The `DOMContentLoaded` event fires when the initial HTML document has been completely loaded
and parsed, without waiting for stylesheets, images, and subframes to finish loading.

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