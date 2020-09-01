---
layout: post
title:  "Difference between Pure and Function React JS component"
date:   2020-03-16 05:30:00 -0700
categories: JavaScript
---

React.PureComponent is similar to React.Component. The difference between them is that React.Component doesn’t implement shouldComponentUpdate(), but React.PureComponent implements it with a shallow prop and state comparison.

Function React component is that which accepts a single “props” (which stands for properties) object argument with data and returns a React element. 

References:
- https://reactjs.org/docs/react-api.html#reactpurecomponent
- https://reactjs.org/docs/components-and-props.html