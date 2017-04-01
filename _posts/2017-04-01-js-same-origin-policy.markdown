---
layout: post
title:  "Same origin policy in JavaScript"
date:   2017-04-01 14:55:12 -0700
categories: javascript
---

The same-origin policy restricts how a document or script loaded
from one origin can interact with a resource from another origin.

Two pages have the same origin if the protocol,
port (if one is specified), and host are the same for both pages.

When using document.domain to allow a subdomain to access its
parent securely, you need to set document.domain to the same value
in both the parent domain and the subdomain. This is necessary
even if doing so is simply setting the parent domain back to
its original value. Failure to do this may result in permission errors.

- References

https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy

http://lucybain.com/blog/2014/same-origin-policy/
