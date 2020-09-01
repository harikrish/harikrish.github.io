---
layout: post
title: REST Principles
categories: HTTP
---

REST stands for Representational State Transfer

5 key principles of REST are -*Give everything a ID
Examples
http://example.com/orders/2007/11
http://example.com/products?color=green

* Link things together
Links help to refer to identifiable things

* Use standard methods
GET- To retrieve a representation. Its idempotent, meaning that has no additional effect if it is called more than once with the same input parameters
PUT - update this resource with this data, or create it at this URI if it’s not there already. Its idempotent.
DELETE - delete a resource. Its idempotent.
POST - create a new resource. Its not idempotent.

* Resources with multiple representations
Provide multiple representations of resources for different needs.

* Communicate statelessly
A server should not have to retain some sort of communication state for any of the clients it communicates with beyond a single request. The most obvious reason for this is scalability — the number of clients interacting would seriously impact the server’s footprint if it had to keep client state.

References:
- https://www.ibm.com/developerworks/webservices/library/ws-restful/
- http://tomayko.com/writings/rest-to-my-wife
- http://www.infoq.com/articles/rest-introduction