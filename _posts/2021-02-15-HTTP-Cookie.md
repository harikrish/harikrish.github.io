---
layout: post
title:  "HTTP Cookie"
date:   2021-02-15 10:53:00 -0700
categories: [HTTP, Web]
---

An HTTP cookie is a small piece of data that a server sends to the user's web browser.
The browser may store it and send it back with later requests to the same server.
Typically, it's used to tell if two requests came from the same browser, keeping a 
user logged-in, for example. It remembers stateful information for the stateless
HTTP protocol.

### Lifetime of a cookie
- Session cookies - They are deleted when the current session ends. 
- Permanent cookies - They are deleted at a date specified by the `Expires` attribute or 
after a period of time specified by the `Max-Age` attribute.

### Cookie security
A cookie with `Secure` attribute is sent to the server only with an encrypted request
over the HTTPS protocol.
A cookie with `HttpOnly` attribute is inaccessiblt to the JavaScript `Document.cookie` API,
it is sent only to the server.

### Cookie scope
The `Domain` attribute specified which hosts are allowed to receive the cookie.
If unspecified, it defaults to the same host that sets the cookie, excluding subdomains.
If `Domain` is specified, then subdomains are always included.
The `Path` attribute indicates a URL path that must exist in the requested URL in order
to send the `Cookie` header. 
The `SameSite` attribute lets servers specify when cookies are sent with cross-origin 
requestes, which provides some protection against cross-site request forgery attacks.

### Third-part cookies
A cookie is associated with a domain. If this domain is the same as the domain of the page
you are on, the cookie is called a first-party cookie. If the domain is different, it is 
a third-party cookie. 

### Cookies and web performance
When a browser sends a HTTP request, the HTTP request headers are usually 400-500 bytes.
Adding a cookie to that will increase the size of the request header. If we add more than 1KB
of cookies to that request, then we exceed 1500bytes, which is the standard maximum transmission unit (MTU)
used by TCP. This means that the HTTP request would span multiple TCP packets, which may result in
multiple round trips and increase the risk of retransmission. This can potentially increase the time to first byte (TTFB)
of the response since it would take longer to make the request. Because of impact of cookie
size on the first flight of requests and responses, it is beneficial to use smaller cookies.
900 bytes seems like a good budget for a total cookie size, which leaves room for other headers such as user-agent.


### References:
- [A re-introduction to HTTP cookies](https://www.valentinog.com/blog/cookies/)
- [Using HTTP cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
- [An analysis of Cookie Sizes on the Web](https://paulcalvano.com/2020-07-13-an-analysis-of-cookie-sizes-on-the-web/)