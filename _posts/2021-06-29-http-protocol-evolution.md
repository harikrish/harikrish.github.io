---
layout: post
title:  "HTTP protocol evolution"
date:   2021-06-29 13:53:00 -0700
categories: [HTTP, Web]
---

HTTP(Hyper Text Transfer Protocol) is the underlying protocol of World Wide Web (www).
Developed by Tim Berners-Leet and his team between 1989-1991.

HTTP has four version - HTTP/0.9, HTTP/1.0, HTTP/1.1, HTTP/2.0.

## HTTP/0.9
HTTP/0.9 request consists of a single line and start with only
possible method `GET` followed by the path to the resource.

{% highlight shell %}
GET /mypage.html
# Example from https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP
{% endhighlight %}

{% highlight shell %}
<HTML>
A very simple HTML page
</HTML>
{% endhighlight %}

## HTTP/1.0
- Status code sent at the beginning of the response.
- HTTP headers introduced for both requests and responses.
- Transmit other documents than plain HTML files.

{% highlight shell %}
GET /mypage.html HTTP/1.0
User-Agent: NCSA_Mosaic/2.0 (Windows 3.1)

200 OK
Date: Tue, 15 Nov 1994 08:12:31 GMT
Server: CERN/3.0 libwww/2.17
Content-Type: text/html
<HTML>
A page with an image
    <IMG SRC="/myimage.gif">
</HTML>

GET /myimage.gif HTTP/1.0
User-Agent: NCSA_Mosaic/2.0 (Windows 3.1)

200 OK
Date: Tue, 15 Nov 1994 08:12:31 GMT
Server: CERN/3.0 libwww/2.17
Content-Type: text/gif
(image content)
# Example from https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP
{% endhighlight %}

## HTTP/1.1
First standardized version of HTTP, published in early 1997.

- Connection can be reused.
- Pipelining, allow a second request before answer for first one is fully transmitted.
- Chunked responses.
- Additional cache control mechanisms.
- Content negotiation.
- Host header added.

{%highlight shell %}
GET /en-US/docs/Glossary/Simple_header HTTP/1.1
Host: developer.mozilla.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://developer.mozilla.org/en-US/docs/Glossary/Simple_header

200 OK
Connection: Keep-Alive
Content-Encoding: gzip
Content-Type: text/html; charset=utf-8
Date: Wed, 20 Jul 2016 10:55:30 GMT
Etag: "547fa7e369ef56031dd3bff2ace9fc0832eb251a"
Keep-Alive: timeout=5, max=1000
Last-Modified: Tue, 19 Jul 2016 00:59:33 GMT
Server: Apache
Transfer-Encoding: chunked
Vary: Cookie, Accept-Encoding
(content)

# Example from https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP
{% endhighlight %}

## HTTP/2
Google's SPDY protocol served as the foundations of the HTTP/2 protocol.
- Its a binary protocol rather than text.
- Its a multiplexed protocol.
- It compresess headers, removes duplication and overhead of data transmitted.
- It allows a server to populate data in a client cache.
The adoption rate is rapid, since having a up-to-date server communicating
with a recent browser is enought to enable its use.

### References
- [Evolution of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
- [Evolution of HTTP](https://medium.com/platform-engineer/evolution-of-http-69cfe6531ba0)
- [Brief history of HTTP](https://hpbn.co/brief-history-of-http/)