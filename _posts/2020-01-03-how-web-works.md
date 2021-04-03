---
layout: post
title:  "How web works ?"
date:   2020-01-03 05:30:00 -0700
categories: [Web, HTTP]
---

What happens when we enter a URL like https://en.wikipedia.org in a browser ?

### DNS Lookup
The browser contacts a server on internet called a DNS server and asks it, "What is the IP of "en.wikipedia.org ?".
DNS server transforms domain names into IP address. For example DNS server response for this case could be "198.35.26.96".

### Connect to IP address and fetch the HTML page
The browser send an `HTTP GET /` HTTP request to the web server running on the computer at that address.
HTTP is a protocol which allows the fetching of resources such as HTML documents. Its the foundation of data
exchange on the web.

### Render HTML web page
The browser takes the HTML response returned by the server and renders it as a web page.
HTML is a martup language, it is the standard for creating web pages.

### References
- [How Web Works](https://github.com/vasanthk/how-web-works)
- [What Happens Under the Hood When You Open a Web Page?](http://tleyden.github.io/blog/2016/09/30/the-lifecycle-of-an-http-request/)
- [Deep Dive of What Happens Under the Hood When You Open a Web Page](http://tleyden.github.io/blog/2016/10/02/deep-dive-of-what-happens-under-the-hood-when-you-open-a-web-page/)
- [What Happens When Yout Type in a URL](https://wsvincent.com/what-happens-when-url/)