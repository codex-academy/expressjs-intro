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

You can combe the above template with this data:

```javascript
var user = {
 author : true,
 firstName : "Jo",
 lastName : "Blogss"
};
```

like this:

```javascript

var templateString = document.querySelector('.entry').innerHTML;

var templateInstance = Handlebars.compile(templateString);

var html = templateInstance(user);

```

results in this html:

{% highlight html %}
{% raw %}
<div class="entry">
    <h1>Joe Bloggs</h1>
</div>{% endraw %}
{% endhighlight %}

> Note that you need to reference the Handlebars library. You can use a link to cdnjs.org like this
{% highlight html %}{% raw %}
<script src="https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/4.0.6/handlebars.js"></script>
{% endraw %}{% endhighlight %}

## Templating using Handlebars

[HandlebarsJS](https://www.npmjs.com/package/handlebars) is built on top of [Mustache](https://www.npmjs.com/package/mustache) templating engine and extends it. Mustache templating aims to be logic-less templating, but that make Mustache hard to use at times.

Read more on [the Mustache website](https://mustache.github.io/mustache.5.html).

Read here about [what are the differences between Mustache.js and Handlebars.js?](http://stackoverflow.com/questions/10555820/what-are-the-differences-between-mustache-js-and-handlebars-js)

## Handlebars helpers

Handlebars comes with a set of built in helpers that makes it easy for one to process data and convert it into a layout. It [supports things like if statements and loops](http://handlebarsjs.com/builtin_helpers.html).
