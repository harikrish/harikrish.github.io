---
layout: post
title:  "Component Composition"
date:   2020-09-25 09:18:00 -0700
categories: [JavaScript, ReactJS]
---

Component composition is where a more "specific" component renders a more "generic"
one and configures it with props.

{% highlight jsx %}

function Button(props) {
    return (
        <button>{props.label}</button>
    )
}

function SignupButton() {
    return (
        <Button label="Signup"/>
    )
}

{% endhighlight %}


### Higher-Order Components
A higher-order component is a function that takes a component and returns a new component.
It composes the original component by wrapping it in a container component. Its a pure
function with zero side-effects. The wrapped component receives all the props of the 
container, along with any new props from the container comopnent.
HOCs are similar to pattern called "container components". Container components are 
part of a strategy of separating responsibility between high-level and low-level concerns.
Containers manage things like subscriptions and state and pass props to components that
handle things like rendering UI. 
HOCs add features to a component. They shouldn't drastically alter its contract. It's
expected that the component returned from a HOC has a similar interface to the wrapped
component.

{% highlight javascript %}

const EnhancedComponent = higherOrderComponent(WrappedComponent);

{% endhighlight %}

### References:
- [Higher-Order Components](https://reactjs.org/docs/higher-order-components.html)
- [Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)