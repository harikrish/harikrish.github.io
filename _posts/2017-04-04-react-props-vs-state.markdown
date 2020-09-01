---
layout: post
title:  "Difference between ReactJS prop vs state"
date:   2017-04-04 15:23:05 -0700
categories: [JavaScript, React]
---

### Props
Props are read only.
Whether a component is defined as a function or a class, it
must never modify its own props. All react component must
act like pure functions with respect to their props.

{% highlight jsx %}

function TitleComponent(props) {
    return <h1>{props.title}</h1>;
}

{% endhighlight %}

### State 
State is similar to props, but its private and fully controlled
by the component.
State is local or encapsulated and its not accessible to
any component other than the one that owns it.
State is changeable.
Do not modify state directly, Instead use setState() function.
State updates may be asynchronous, to fix it, use second form of
setState() that accepts a function rather than a object.
React calls render method after state is changed to learn what
should be on the screen.

{% highlight jsx %}

class MyForm extends React.Component {
    constructor(props) {
        super(props);
        this.state = {name: "Hello World"};
    }

    render() {
        return (
            <form>
                <input type="text" 
                    value={this.state.name} 
                    onChange={this.handleOnChange.bind(this)}/>
            </form>
        )       
    }

    handleOnChange(e) {
        this.setState({
            name: e.target.value
        })
    }
}

{% endhighlight %}

#### References
- [Components and Props](https://facebook.github.io/react/docs/components-and-props.html)
- [State and Lifecycle](https://facebook.github.io/react/docs/state-and-lifecycle.html)
- [ReactJS: Props vs. State](http://lucybain.com/blog/2016/react-state-vs-pros/)
