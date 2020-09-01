---
layout: post
title:  "What is a React Pure Component ?"
date:   2017-04-25 14:01:00 -0700
categories: [React, JavaScript]
---

If React components `render()` function renders the same result given the same
props and state , you can use `PureComponent` for a performance boost.

`PureComponent`'s `shouldComponentUpdate()` function only shallow compares the objects.
Also its skips prop updates for the whole component subtree. So need to make 
sure that all the children components are also "pure".

Best use case for `PureComponent` are presentational components which have no 
child components and no dependencies on the global state in the application.

{% highlight jsx %}

class MyComponent extends React.PureComponent {
    render() {
        return (
            <h1>Hello World!</h1>
        );
    }
}

{% endhighlight %}

### References
- [React Top-Level API](https://facebook.github.io/react/docs/react-api.html#react.purecomponent)
- [Why and How to Use PureComponent in React.js](https://60devs.com/pure-component-in-react.html)