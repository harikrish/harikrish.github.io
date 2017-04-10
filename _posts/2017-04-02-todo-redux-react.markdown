---
layout: post
title:  "TODO example with React and Redux"
date:   2017-04-02 16:42:48 -0700
categories: React Redux JavaScript
---

This article explains how to create a simple React Todo example using Redux.

- Install create-react-app

https://github.com/facebookincubator/create-react-app

{% highlight shell %}

npm install -g create-react-app

{% endhighlight %}

- Create todo app using create-react-app command line.

{% highlight shell %}

create-react-app todo-react-redux

{% endhighlight %}

- Create the component, container, reducer, action folders.

{% highlight shell %}

cd todo-react-redux
mkdir components containers actions reducers

{% endhighlight %}

- Install required Redux and dependency packages

{% highlight shell %}

 npm install --save redux
 npm install --save react-redux

{% endhighlight %}


- Create the components Todo.js, TodoList.js, Footer.js, Link.js (https://github.com/harikrish/todo-react-redux/tree/master/src/components)

- Create the container components AddTodo.js, FilterLink.js, VisibleTodoList.js (https://github.com/harikrish/todo-react-redux/tree/master/src/containers)

- Create the reducers todos.js, visibilityFilter.js (https://github.com/harikrish/todo-react-redux/tree/master/src/reducers)

- Create the actions (https://github.com/harikrish/todo-react-redux/tree/master/src/actions)

- Update App.js, index.js (https://github.com/harikrish/todo-react-redux/tree/master/src)

- Run the server

{% highlight shell %}

npm start

{% endhighlight %}
