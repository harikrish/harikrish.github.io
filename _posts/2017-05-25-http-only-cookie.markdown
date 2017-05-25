---
layout: post
title:  "What is a HttpOnly cookie?"
date:   2017-05-25 11:20:00 -0700
categories: HTTP
---

HttpOnly is an additional flag included in Set-Cookie HTTP response
header. Using the HttpOnly flag when generating a cookie helps 
mitigate the risk of client side script accessing the protected cookie
(if the browser supports it).

References
- https://www.owasp.org/index.php/HttpOnly