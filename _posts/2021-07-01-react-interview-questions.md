---
layout: post
title:  "React JS Interview Questions"
date:   2021-07-01 16:18:00 -0700
categories: [JS, React]
---

## What is JSX?
JSX is a XML like syntax extension to ECMAScript (JavaScript XML).

{% highlight javascript %}
const element = <h1>Hello, world!</h1>;
{% endhighlight %}

## What are the difference between a class component and functional component?
If a component needs state or lifecycle methods use class component otherwise
use functional component.

## What are Pure components?
React.PureComponent is similar to React.Component. The difference
between them is that React.Component doesn't implement shouldComponentUpdate,
but React.PureComponent implements it with a shallow prop and state
comparison.

## What is React.memo?
React.memo is a higher order component.
If your component renders the same result given the same props,
you can wrap it in a call to React.memo for performance boost.

## What is the difference between state and props?
props and state are both plain JavaScript objects.
props get passed to the component whereas state is
managed withing the component.

## What are synthetic events in React?
SyntheticEvent is a cross-browser wrapper around the browser's
native event. It's API is same as the browser's native event.

## What is Virtual DOM?
The Virtual DOM is an in-memory representation of the real DOM.
Whenever any underlying data changes, the entire UIR is
re-rendered in Virtual DOM representations. Then the difference
between the previous DOM representation and new is calculated.
Once the calculations are done, the real DOM will be updated
with only the things that have actually changed.

## What is "React Fiber"?
Fiber is the new reconcillation engine in React 16. Its main
goal is to enable incremental rendering of the virtual DOM.

## What are Controlled Components?
With a controlled component, the input's value is always
driven by the React state.

## What are Uncontrolled Components?
An uncontrolled component keeps the source of truth in
the DOM.

## What are Higher-Order Components?
A higher-order component is a function that takes a component
and returns a new component.

## What is ReactDOM?
The `react-dom` package provides DOM-specific methods that can
be used at the top level of the app.

## What are Fragments?
Fragments let you group a list of children without adding extra
nodes to the DOM.

## What is Context?
Context provides a way to pass data through the component tree
without having to pass props down manually at every level.

## What are Keys?
Keys help React to identify which items have changed, are added,
or are removed. Keys should be given to elements inside the array
to give the elements a stable identity.

## What are Refs?
Refs provide a way to access DOM nodes or React elements created in the 
render method.

## What is Ref forwarding?
Ref forwarding is a technique for automatically passing a `ref` through
a component to one of its children.

## What is ReactDOMServer?
The `ReactDOMServer` object enables you to render components to static
markup.

## What are Portals?
Portals provide a first-class way to render children into a DOM node
that exists outside the DOM hierarchy of the parent component.

## What are the lifecycle methods of React?
Before React 16.3
- componentWillMount - Is invoked just before mounting occurs.
Its called before `render()`.
- componentDidMount - Is invoked immediately after a component is mounted.
- componentWillRecieveProps - Is invoked before a mounted component receives
new props. 
- shouldComponentUpdate - To let React know if a component's output is not
affected by the current change in state or props.
- componentWillUpdate - Is invoked just before rendering new props or state
are being received.
- componentDidUpdate - Is invoked immediately after updating occurs.
- componentWillUnMount - Is invoked immediately before component is unmounted
and destroyed.
- render - Is invoked to render component
- constructor - Is called before component is mounted.

React 16.3+
- getDerivedStateFromProps - Is invoked right before calling the render method,
both on the initial mount and on subsequent updates.
- getSnapshotBeforeUpdate - Is invoked right before the most recently rendered
output is committed to e.g. the DOM.

## What are hooks?
Hooks are a new addition in React 16.8. They let you use state and other features
without writing a class.

## What are default props?
`defaultProps` can be defined as a property on the component class itself, to set
the default props for the class.

## What are PropTypes?
React has some built-in typechecking abilities. To run typechecking on the props
for a component, you can assign the special `propTypes` property.

### References
- [React Interview Questions & Answers](https://github.com/sudheerj/reactjs-interview-questions)
- [Frequently asked: React JS Interview Questions and Answers](https://vigowebs.medium.com/frequently-asked-react-js-interview-questions-and-answers-36f3dd99f486)
- [21 Essential React.js Interview Questions *](https://www.toptal.com/react/interview-questions)
- [https://dev.to/suprabhasupi/react-redux-interview-questions-with-answers-13ba](https://dev.to/suprabhasupi/react-redux-interview-questions-with-answers-13ba)
- [React Functional Components VS Class Components](https://medium.com/wesionary-team/react-functional-components-vs-class-components-86a2d2821a22)
- [Component State](https://reactjs.org/docs/faq-state.html)
- [Virtual DOM and Internals](https://reactjs.org/docs/faq-internals.html)
- [Context](https://reactjs.org/docs/context.html)
- [Keys](https://reactjs.org/docs/lists-and-keys.html#keys)
- [Refs and the DOM](https://reactjs.org/docs/refs-and-the-dom.html)
- [Forwarding Refs](https://reactjs.org/docs/forwarding-refs.html)
- [React.Component](https://reactjs.org/docs/react-component.html)
- [State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
- [React Lifecycle](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)