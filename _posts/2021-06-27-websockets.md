---
layout: post
title:  "WebSockets"
date:   2021-06-27 11:50:00 -0700
categories: [HTTP, Web]
---

WebSocket is a technology that allows a client to establish two way communication
with the server. 

WebSockets allows establishing a persistent connection between the web browser
and server, so that both parties can start sending data at any time.

WebSocket allows to build real time communication apps.

On the frontend, example code to establish a connection to a WebSocket
enabled server.
{% highlight javascript %}
const socket = new WebSocket('ws://localhost:8080');
socket.addEventListener('open', function(event) {
    socket.send('Hello Server!');
});

socket.addEventListener('message', function(event) {
    console.log('Message from server', event.data);
});

socket.addEventListener('close', function(event) {
    console.log('The connection has been closed');
});
// Example code from https://stackoverflow.blog/2019/12/18/websockets-for-fun-and-profit/
{% endhighlight %}

On the server, example code to open a connection and listen for messages.
{% highlight javascript %}
const WebSocket = require('ws');
const ws = new WebSocket.Server({ port: 8080});
ws.on('connection', function connection(wsConnection) {
    wsConnection.on('message', function incoming(message) {
        console.log('server recieved : ${message}');
    });

    wsConnection.send('got your message!');
});
// Example code from https://stackoverflow.blog/2019/12/18/websockets-for-fun-and-profit/
{% endhighlight %}

### References
- [The Problem: Low Latency Client-Server and Server-Client Connections](https://www.html5rocks.com/en/tutorials/websockets/basics/)
- [WebSockets for fun and profit](https://stackoverflow.blog/2019/12/18/websockets-for-fun-and-profit/)
- [WebSockets - A Conceptual Deep Dive](https://ably.com/topic/websockets)