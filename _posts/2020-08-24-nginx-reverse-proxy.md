---
layout: post
title:  "Nginx Reverse proxy for cross domains"
date:   2020-08-24 10:24:00 -0700
categories: [HTTP]
---

A reverse proxy is a server that sits in front of web servers and forwards
client request to those web servers. 

Use case:
If we try to access URL http://example.com:8080/api from webpage at http://example.com
due to browser cross domain restrictions we will see CORS errors.

To solve, we can setup Nginx reverse proxy server, so that , we can request URL
http://example.com/api from webpage at http://example.com and the reverse proxy server would
take care of forwarding the request to server running at port 8080.

{% highlight conf %}
server {
    listen       80;
    listen  [::]:80;
    server_name  localhost;

    location / {
        root   /usr/share/nginx/html;
        index  index.html index.htm;
    }

    location /api {
        proxy_set_header HOST $host;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;

        proxy_pass http://127.0.0.1:8080;
    }
}
{% endhighlight %}

To pass a request to an HTTP proxied server, the `proxy_pass` directive is specified
inside a location.

- `$host` - This variable is set, in order of preference to: the host name from the request line itself,
the "Host" header from the client request, or the server name matching the request.
- `$scheme` - The schema of the original request. 
- `X-Forwarded-Proto` - header gives the proxied server information on the schema of the original request.
- `X-Real-IP` - It is set to the IP address of the client.
- `$proxy_add_x_forwarded_for` - This variable takes the value of original `X-Forwarded-For` header retrieved
from the client and adds the Nginx server IP address to the end.


### References:
- [What Is A Reverse Proxy?](https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/)
- [NGINX Reverse Proxy](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/)
- [Avoid CORS with Nginx proxy_pass](http://oskarhane.com/avoid-cors-with-nginx-proxy_pass/)
- [how to use nginx as reverse proxy for cross domains
](https://stackoverflow.com/questions/36974100/how-to-use-nginx-as-reverse-proxy-for-cross-domains)
- [Understanding Nginx HTTP Proxying, Load Balancing, Buffering, and Caching](https://www.digitalocean.com/community/tutorials/understanding-nginx-http-proxying-load-balancing-buffering-and-caching)
- [3 Ways to Fix the CORS Error — and How the Access-Control-Allow-Origin Header Works](https://medium.com/@dtkatz/3-ways-to-fix-the-cors-error-and-how-access-control-allow-origin-works-d97d55946d9)