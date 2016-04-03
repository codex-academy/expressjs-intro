---
layout: default
---

# Middleware

One extends ExpressJS functionality using middleware.

We will look at middleware to:

    * process form variables;
    * to handle http sessions;
    * to display flash messages.

## Form Variables

To process variables sent from Http form posts add the [body-parser](https://www.npmjs.com/package/body-parser) middleware to ExpressJS.

This will enable the `req.body` variable in ExpressJS route handlers.

## Http Sessions

Storing state between Http calls.

Http is a stateless protocol, Http Sessions allow one to store variables between http calls.

To enable Http Sessions in ExpressJS one need to add the [express-session](https://www.npmjs.com/package/express-session) middleware to ExpressJS.

This will enable the `req.session` variable in ExpressJS route handlers.

## Flash messages

An easy way to display messages after a redirect is to add the [express-flash](https://www.npmjs.com/package/express-flash) middleware.

This will enable the `req.flash` variable in ExpressJS route handlers.

Add a flash message like this:

```javascript
app.get('/the-route', function (req, res) {
    req.flash('info', 'Flash Message Added');
    res.redirect('/');
});
```

This will add a variable on can use in handlebars templates like this:

{% highlight html %}
{% raw %}
<div class="entry">
    <h1> {{messages.info}}</h1>
</div>{% endraw %}
{% endhighlight %}
