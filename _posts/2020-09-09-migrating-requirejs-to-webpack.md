---
layout: post
title:  "Migrating from RequireJS to Webpack"
date:   2020-09-09 14:09:00 -0700
categories: [JavaScript]
---

### Minimal amount of changes in actual code
Webpack compiler can understand modules written as ES2015 modules, CommonJS or AMD.
Existing code using `define()` function doesn't need modification.

### Migrating Require.js config to Webpack config
The first thing to do when converting from Require.js to Webpack is to take your whole Require.js configuration file (requirejs_config.js) and convert it into Webpack configuration file (webpack.config.js).

#### Module Path Resolution
Help Webpack to find your module files. 

{% highlight javascript %}
// Webpack
    {
        resolve: {
            modules: [
                'app/assets/javascripts',
                'app/assets/stylesheets'
            ],
        }
    }
{% endhighlight %}

#### NPM in place of Bower components
You can use NPM in place of Bower components , since we can configure easily in Webpack to load NPM dependencies

{% highlight javascript %}
// Webpack
    {
        resolve: {
            modules: [
                'app/assets/javascripts',
                'app/assets/stylesheets',
                'node_modules'
            ],
        }
    }
{% endhighlight %}

#### Aliases
Migrate Require.js `paths` to webpack `alias`

{% highlight javascript %}
// Require.js
    {
        paths: {
            'foundation-core': './foundation/js/foundation/foundation',
            'foundation-abide': './foundation/js/foundation/foundation.abide',
            'foundation-accordion': './foundation/js/foundation/foundation.accordion'
        }
    }
{% endhighlight %}

{% highlight javascript %}
// Webpack
    {
        resolve: {
            alias: { 
                'foundation-core': 'foundation-sites/js/foundation/foundation',
                'foundation-abide': 'foundation-sites/js/foundation/foundation.abide',
                'foundation-accordion': 'foundation-sites/js/foundation/foundation.accordion'
            }
        }
    }
{% endhighlight %}

### Shim
Require.js shim takes modules that are not AMD compatible and makes them compatible.

{% highlight javascript %}
//Require.js
    {
        'shim': {
            'foundation-core': { 'deps': ['jquery'] },
            'foundation-abide': { deps: ['foundation-core'] }
        }
    }
{% endhighlight %}

{% highlight javascript %}
//Webpack
    {
        resolve: {
            module: {
                rules: [{
                    test: /foundation-core/,
                    use: ['imports-loader?jquery']
                },
                {
                    test: /foundation-abide/,
                    use: ['imports-loader?foundation-core']
                }]
            }
        }
    }
{% endhighlight %}

### References:
- [From Require.js to Webpack - Part 2](https://gist.github.com/xjamundx/b1c800e9282e16a6a18e)
- [Migrating Gumroad from RequireJS to webpack](https://blog.bigbinary.com/2018/12/12/migrating-gumroad-from-requirejs-to-webpack.html)
- [Migration from Require.js to Webpack 2](https://medium.com/@ArtyomTrityak/migration-from-require-js-to-webpack-2-a733a4366ab5)
- [Migrate from RequireJS to webpack](https://espressoprogrammer.com/migrate-requirejs-webpack/)
- [Shimming](https://webpack.js.org/guides/shimming/)
- [define() function](https://github.com/amdjs/amdjs-api/wiki/AMD#define-function-)
- [WHY AMD?](https://requirejs.org/docs/whyamd.html)
- [Resolve](https://webpack.js.org/configuration/resolve/)
- [imports-loader](https://webpack.js.org/loaders/imports-loader/)