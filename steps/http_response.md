---
layout: default
---

# Http Response

The Http Response object is all about sending output to the browser.

Some of the methods it supports are:

* res.send
* res.redirect
* res.render

## send

To send some data to the browser use `res.send`. It's the simplest way to send data to the client.

## render

```javascript
app.post('/add_product', function(req, res){
 res.render('product', {product :  data});
});
```

In the example above the response object is used to render a template to the client.

## redirect

To redirect to another route look at the example below:

```javascript
// redirect to the login route
res.redirect("/login");
```
