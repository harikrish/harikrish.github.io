---
layout: post
title:  "React PropTypes"
date:   2020-08-11 11:59:00 -0700
categories: [JavaScript, React]
---

React PropTypes help with typechecking on the props for a component.
When a invalid value is provided for a prop,a warning will be shown
in the JavaScript console. PropTypes is only checked in development
mode.

{% highlight jsx %}
import PropTypes from 'prop-types';

class MyHeader extends React.Component {
    render() {
        return (
            <h1>{this.props.value}</h1>
        )
    }
}

MyHeader.propTypes = {
    value: PropTypes.string.isRequired
};

{% endhighlight %}

### References:
- [Typechecking With PropTypes](https://reactjs.org/docs/typechecking-with-proptypes.html)