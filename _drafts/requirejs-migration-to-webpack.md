---
layout: post
title:  "How to migrate RequireJS project to Webpack project"
date:   2020-01-03 05:30:00 -0700
categories: javascript
---


https://blog.bigbinary.com/2018/12/12/migrating-gumroad-from-requirejs-to-webpack.html
https://medium.com/@ArtyomTrityak/migration-from-require-js-to-webpack-2-a733a4366ab5
https://espressoprogrammer.com/migrate-requirejs-webpack/
https://gist.github.com/xjamundx/b1c800e9282e16a6a18e
https://webpack.js.org/guides/shimming/

{% highlight shell %}

npm install webpack --save-dev
npm install webpack-cli --save-dev

{% endhighlight shell %}

Create webpack.config.js

{% highlight javascript %}

const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
};

{% endhighlight  javascript %}

https://github.com/flarnie/webpack_rails_demo
https://medium.com/hackernoon/the-100-correct-way-to-split-your-chunks-with-webpack-f8a9df5b7758
https://medium.com/dailyjs/webpack-4-splitchunks-plugin-d9fbbe091fd0
https://gist.github.com/xjamundx/b1c800e9282e16a6a18e
https://wanago.io/2018/06/04/code-splitting-with-splitchunksplugin-in-webpack-4/
https://reinteractive.com/posts/213-rails-with-webpack-why-and-how
http://clarkdave.net/2015/01/how-to-use-webpack-with-rails/

https://github.com/webpack/webpack/issues/240