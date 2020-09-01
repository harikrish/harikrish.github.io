---
layout: post
title:  "React Hooks"
date:   2020-03-26 06:35:48 -0700
categories: [JavaScript, React]
---

Hooks let you use more of React’s features without classes.
Hooks embrace functions, but without sacrificing the practical spirit of React. 

{% highlight jsx %}
// code from https://reactjs.org/docs/hooks-overview.html

// State Hook example
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

{% endhighlight %}

{% highlight jsx %}
// code from https://reactjs.org/docs/hooks-overview.html

// Effect Hook example
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
{% endhighlight %}

References:
- [Introducing Hooks](https://reactjs.org/docs/hooks-intro.html)