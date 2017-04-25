---
layout: post
title:  "What is a React Pure Component ?"
date:   2017-04-25 14:01:00 -0700
categories: ReactJS JavaScript
---

If React components render() function renders the same result given the same
props and state , you can use PureComponent for a performance boost.

PureComponents shouldComponentUpdate() function only shallow compares the objects.
Also its skips prop upates for the whole component subtree.

References

- https://facebook.github.io/react/docs/react-api.html#react.purecomponent
- https://60devs.com/pure-component-in-react.html