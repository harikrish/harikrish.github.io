---
layout: post
title:  "What is NODE_ENV in Node.js"
date:   2017-05-03 10:45:00 -0700
categories: [JavaScript, NodeJS]
---

NODE_ENV is an environment variable made popular by the Express.js
framework. It is specifically used to state whethere a particular
environment is production or development.

{% highlight JavaScript %}
var environment = process.env.NODE_ENV
{% endhighlight %}


References
- http://stackoverflow.com/questions/16978256/what-is-node-env-in-express