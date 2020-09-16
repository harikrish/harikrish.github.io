---
layout: post
title:  "React server side rendering"
date:   2020-09-15 16:45:00 -0700
categories: [JavaScript, React]
---

React JS , provides `ReactDOMServer` object which
enables to render components to static markup. Typically,
it's used on a Node server.

{% highlight javascript %}
import ReactDOMServer from 'react-dom/server';

ReactDOMServer.renderToString(element)
{% endhighlight %}

Using this method we can generate HTML on the server
and serve it to the browser. This allows for faster
page loads and also allows search engines to crawl
the page for SEO purposes.

### References:
- [ReactDOMServer](https://reactjs.org/docs/react-dom-server.html)
- [Server-Side React Rendering](https://css-tricks.com/server-side-react-rendering/)
- [How to Enable Server-Side Rendering for a React App](https://www.digitalocean.com/community/tutorials/react-server-side-rendering)