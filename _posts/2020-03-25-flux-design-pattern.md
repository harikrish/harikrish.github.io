---
layout: post
title:  "Flux pattern"
date:   2020-03-25 06:35:48 -0700
categories: JavaScript
---

Flux is the application architecture that Facebook uses for building client-side web applications. It complements React's composable view components by utilizing a unidirectional data flow. 

Flux applications have three major parts: the dispatcher, the stores, and the views (React components).

When a user interacts with a React view, the view propagates an action through a central dispatcher, to the various stores that hold the application's data and business logic, which updates all of the views that are affected. This works especially well with React's declarative programming style, which allows the store to send updates without specifying how to transition views between states.

Control is inverted with stores: the stores accept updates and reconcile them as appropriate, rather than depending on something external to update its data in a consistent way. Nothing outside the store has any insight into how it manages the data for its domain, helping to keep a clear separation of concerns.

References:
- https://facebook.github.io/flux/docs/in-depth-overview/
