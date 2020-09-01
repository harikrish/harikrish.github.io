---
layout: post
title:  "What are Functional components in React JS ?"
date:   2017-04-04 13:27:15 -0700
categories: [JavaScript, React]
---

The simplest way to define a component is to write a JavaScript function.
The function accepts a single "props" object and returns a React element.
Such components are called Functional components because the are literally
JavaScript functions.

{% highlight jsx %}
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
{% endhighlight %}

{% highlight jsx %}
// A function component using an ES2015 (ES6) arrow function:
var Aquarium = (props) => {
  var fish = getFish(props.species);
  return <Tank>{fish}</Tank>;
};

// Or with destructuring and an implicit return, simply:
var Aquarium = ({species}) => (
  <Tank>
    {getFish(species)}
  </Tank>
);

// Then use: <Aquarium species="rainbowfish" />
{% endhighlight %}

These components behave just like a React class with only a render method defined.
Since no component instance is created for a function component, 
any ref added to one will evaluate to null. Function components do not have lifecycle methods, 
but you can set .propTypes and .defaultProps as properties on the function.

Advantage of Functional components is that they are much easier to read and test 
because they are plain JavaScript functions without state or lifecycle-hooks.
This pattern is designed to encourage the creation of these simple components 
that should comprise large portions of apps. 

### Reference:
- [Components and Props](https://facebook.github.io/react/docs/components-and-props.html)
- [Functional vs Class-Components in React](https://medium.com/@Zwenza/functional-vs-class-components-in-react-231e3fbd7108)
- [Stateless function components](https://reactjs.org/blog/2015/10/07/react-v0.14.html#stateless-functional-components)