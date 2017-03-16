---
layout: default
---

# Flash messages

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
