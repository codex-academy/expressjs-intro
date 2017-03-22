---
layout: default
---

# Static files

For ExpressJS to serve static files such as html, css and client side JavaScript some middleware needs to be added.

The ExpressJS module comes with the `static` middleware module.

In your ExpressJS project you can expose a folder calles `public` as a static folder like this.

```javascript
app.use(express.static('public'));
```

You can now add all your css, html and JavaScript files that you want to access from your routs into the `public` folder. You can add other folders as well. Just be sure to expose them with a similar middleware call.
