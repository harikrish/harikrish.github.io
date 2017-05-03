---
layout: post
title:  "What is process.env in Node.js"
date:   2017-05-03 10:00:00 -0700
categories: JavaScript Node.js
---

In Node.js, you can retrieve environment variables by key from 
process.env object.

{% highlight shell %}
node -p process.env
node -p process.env.HOME
{% endhighlight %}


References
- http://stackoverflow.com/questions/15058954/node-js-is-there-any-documentation-about-the-process-env-variable
- https://nodejs.org/api/process.html#process_process_env
- https://davidwalsh.name/node-environment-variables