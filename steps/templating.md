---
layout: default
---
# Templates

To combine data and html we use a template engine.

## Templating using Handlebars example

We will be using `handlebars` as our template engine, it combines data with templates to render information.

A typical handlebars template look likes this

{% highlight html %}
{% raw %}
<div class="entry">
  {{#if author}}
    <h1> {{firstName}} {{lastName}}</h1>
  {{/if}}
</div>{% endraw %}
{% endhighlight %}

combining the above template with this data:

```javascript
var user = {
 author : true,
 firstName : "Jo",
 lastName : "Blogss"
};
```

results in this html:

{% highlight html %}
{% raw %}
<div class="entry">
    <h1>Joe Bloggs</h1>
</div>{% endraw %}
{% endhighlight %}

## Templating using Handlebars

[HandlebarsJS](https://www.npmjs.com/package/handlebars) is built on top of [Mustache](https://www.npmjs.com/package/mustache) templating engine and extends it. Mustache templating aims to be logic-less templating, but that make Mustache hard to use at times.

Read more on [the Mustache website](https://mustache.github.io/mustache.5.html).

Read here about [what are the differences between Mustache.js and Handlebars.js?](http://stackoverflow.com/questions/10555820/what-are-the-differences-between-mustache-js-and-handlebars-js)

## Handlebars helpers

Handlebars comes with a set of built in helpers that makes it easy for one to process data and convert it into a layout. It [supports things like if statements and loops](http://handlebarsjs.com/builtin_helpers.html).

## View Engine

To make it easy to use Handlebars templates in ExpressJS we configure Handlebars as a view engine in ExpressJS. Using the [express-handlebars](https://www.npmjs.com/package/express-handlebars) module.

Configure it like this :

```javascript
app.engine('handlebars', exphbs({defaultLayout: 'main'}));
app.set('view engine', 'handlebars');
```

Then use it like this:

```javascript
var data_for_template = {};
res.render('template_name', data_for_template);
```

## Useful links:

* [Loading JSON files using require](https://nodejs.org/api/modules.html#modules_file_modules)
* [Express JS](http://expressjs.com/)
* [Handlebars JS](http://handlebarsjs.com/)
* [Mustache](https://mustache.github.io/)
