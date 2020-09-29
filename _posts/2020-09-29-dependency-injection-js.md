---
layout: post
title:  "Dependency Injection in JavaScript"
date:   2020-09-29 10:40:00 -0700
categories: [JavaScript]
---

Dependency Injection is a pattern where instead of creating or requiring 
dependencies directly inside a module, we pass them as paramaeters or reference.

{% highlight javascript %}
// foo.js
export default class Foo {
    print() {
        console.log('Hello world!');
    }
}

//baz.js
import Foo from './foo.js';

export default class Baz {
    constructor() {
        this.foo = new Foo();
    }
}

//app.js
import Baz from './baz.js';

let b = new Baz();
{% endhighlight %}

{% highlight javascript %}
// Using Dependecy Injection
// Updated baz.js
export default class Baz {
    constructor(foo) {
        this.foo = foo;
    }
}

//app.js
import Foo from './foo.js';
import Baz from './baz.js';

let b = new Baz(new Foo()); // Foo instance is passed as parameter to Baz
{% endhighlight %}

### Benefits
- Unit testing - Avoid need for stubbing
- Flexibility - Freedom to change implementation at any point


### References:
- [Dependency Injection in JavaScript
](https://www.devbridge.com/articles/dependency-injection-in-javascript/)
- [JavaScript dependency injection in Node.js – friends or foes?](https://tsh.io/blog/dependency-injection-in-node-js/)
- [Dependency Injection & Inversion Explained](https://khalilstemmler.com/articles/tutorials/dependency-injection-inversion-explained/)
- [Handling dependencies](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Main_features#Handling_dependencies)