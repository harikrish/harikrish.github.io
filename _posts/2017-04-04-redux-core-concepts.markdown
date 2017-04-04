---
layout: post
title:  "Core concepts of Redux"
date:   2017-04-04 13:27:15 -0700
categories: JavaScript
---

- Store

The state of your whole application is stored in an
Object tree within a single store.
This object is like a 'model' except there are no setters.
This is so that different parts of the code can't change
the state arbitrarily, causing hard to reproduce bugs.


- Action

The only way to change the state is to emit an action,
an object describing what happened.
Enforcing that every change is described as an action lets
us have a clear understanding of what's going on in the app.


- Reducer

To specify how a state tree is transformed by actions,
you write pure reducers.
Its just a function which takes state and action as arguments,
and returns the next state of the app.

- References

http://redux.js.org/docs/introduction/CoreConcepts.html

http://redux.js.org/docs/introduction/ThreePrinciples.html
