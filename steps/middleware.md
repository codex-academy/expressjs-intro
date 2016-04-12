---
layout: default
---

# Middleware

You can extend ExpressJS functionality using middleware.

We will look at middleware to:

* process form variables;
* to handle HTTP sessions;
* to display flash messages.

## Form Variables

To process variables sent from HTTP form posts add the [body-parser](https://www.npmjs.com/package/body-parser) middleware to ExpressJS.

This will enable the `req.body` variable in ExpressJS route handlers.

## HTTP Sessions

Storing state between HTTP calls.

HTTP is a stateless protocol, HTTP Sessions allow one to store variables between HTTP calls.

To enable HTTP Sessions in ExpressJS one need to add the [express-session](https://www.npmjs.com/package/express-session) middleware to ExpressJS.

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

This will add a variable you can use in handlebars templates like this:

```html
{% raw %}
<div class="entry">
    <h1>{{messages.info}}</h1>
</div>
{% endraw %}
```
