---
layout: default
---
# Templates

To combine data and html we use a template engine.

## Templating using Handlebars

We will be using `handlebars` as our template engine, it combines data with templates to render information.

A typical handlebars template look likes this

```handlebars
<div class="entry">
  {{#if author}}
    <h1> {{firstName}} {{lastName}}</h1>
  {{/if}}
</div>
```

Combining the above with data like this:

```javascript
var user = {
 author : true,
 firstName : "Jo",
 lastName : "Blogss"
};
```

results in a html enriched with some data.

[HandlebarsJS](https://www.npmjs.com/package/handlebars) is built on top of [Mustache](https://www.npmjs.com/package/mustache) templating engine and extends it. Mustache templating aims to be logic-less templating, but that make Mustache hard to use at times.

Read more on [the Mustache website](https://mustache.github.io/mustache.5.html).

Read here about [what are the differences between Mustache.js and Handlebars.js?](http://stackoverflow.com/questions/10555820/what-are-the-differences-between-mustache-js-and-handlebars-js)

## Handlebars helpers

Handlebars comes with a set of built in helpers that makes it easy for one to process data and convert it into a layout. It [supports things like if statements and loops](http://handlebarsjs.com/builtin_helpers.html).

http://handlebarsjs.com/builtin_helpers.html

## Combining templates & data

As we need to display the data in the web browser we use the templates, which is how we would like the data to be displayed, with what needs to be displayed, which is the data.

It goes like this:

```
template + data = web page
```

To combine templates and data in Express JS we configure Handlebars as a view engine in ExpressJS. Using this module : [Node module that is combining Express JS and Handlebars](https://www.npmjs.com/package/express-handlebars).

## Useful links:

* [Loading JSON files using require](https://nodejs.org/api/modules.html#modules_file_modules)
* [Express JS](http://expressjs.com/)
* [Handlebars JS](http://handlebarsjs.com/)
* [Mustache](https://mustache.github.io/)
