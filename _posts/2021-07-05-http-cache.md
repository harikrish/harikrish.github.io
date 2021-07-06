---
layout: post
title:  "HTTP Cache"
date:   2021-07-05 17:22:00 -0700
categories: [HTTP, Web]
---

HTTP Cache improves performance of web sites and applications by reusing
previously fetchted resources.


## Cache-Control header
The server can return a `Cache-Control` directive to specify how, and for
how long, the browser and other intermediate caches should cache the
individual response.

- No caching
`Cache-Control: no-store`
This instructs the browser and other intermediate caches (like CDNs)
to never store any version of the file.

- Cache but revalidate
`Cache-Control: no-cache`
This instructs the browser that it must revalidate with the server
every time before using a cached version of the URL.

- Private and public caches
`Cache-Control: private`
Browser can cache the file but intermediate caches cannot.
`Cache-Control: public`
The response can be stored by any cache.

- Expiration
`Cache-Control: max-age=31536000`
The maximum amount of time in which a resource will be considered
fresh. This directive is relative to the time of request, and 
overrides the Expires header (if set).

- Validation
`Cache-Control: must-revalidate`
The cache must verify the status of stale resources before using
it and expired ones should not be used.

## ETags
The ETag (or Entity Tag) works in a similar way to the `Last-Modified` 
header except its value is a digest of the resources contents (for instance,
an MD5 Hash). This allows the server to identify if the cached contents
of the resource are different to the most recent version.
If the Etag header was part of the response for a resource, the client
can issue an `If-None-Match` in the header of future requests - in order
to validate the cached resource.

## Last-Modified
This header servers the same purpose as `ETag`, but uses a time-bsaed
strategy to determine if a resource has changed, as opposed to the 
content-based strategy of `ETag`. If the `Last-Modified` header is
present in a response, then the client can issue an `If-Modified-Since`
request header to validate the cached document.

### References
- [HTTP caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
- [HTTP Cache](https://web.dev/http-cache/)
- [Increasing Application Performance with HTTP Cache Headers](https://devcenter.heroku.com/articles/increasing-application-performance-with-http-cache-headers)