---
layout: post
title:  "React Default Prop Values"
date:   2020-08-11 16:37:00 -0700
categories: [JavaScript, React]
---

React Default Props values ensure that the prop  will have a value if it was not 
specified by the parent component.

{% highlight jsx %}
class BazComponent extends React.Component {
    render {
        <div> Hello {this.props.value}!<div>
    }
}

BazComponent.defaultProps = {
    value: 'World'
};
{% endhighlight %}

{% highlight jsx %}
<BazComponent/> // Renders "Hello World!"
{% endhighlight %}