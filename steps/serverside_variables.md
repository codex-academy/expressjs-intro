---
layout: default
---

## Server side variables

Express route callbacks always take two parameters req and res.

Those two variables are HttpRequest (req) and HttpResponse (res) respectively:

# Http Response

The HttpRequest object is all about sending output to the browser.

Some of the methods it supports are:

* res.send
* res.redirect
* res.render

Here is a quick example:

```javascript
app.post('/add_product', function(req, res){
 res.render('product', {product :  data});
});
```

In the example above the response object is used to render a template to the client.

```javascript
// redirect to the login route
res.redirect("/login");
```

# Http Request

The HttpRequest object is all about gathering input from the browser.

There are 3 ways to input data from the request object:

* URL paramaters using `req.params`;
* Query parameters using `req.query`;
* HTML forms parameters using `req.body`


```javascript
app.post('/add_product', function(req, res){
 var formData = req.body;
 console.log(formData.product_name);
 res.render('product', {product_name :  formData.product_name});
});
```

## HTML forms parameters

It reads the form data, prints it to the console and sends it to the template to be rendered back to the client.
This example is only reading one field, but you can read all the fields that are being sent from the form to the route.

**Note:*** For form variables to work in Express you need to configure some middleware that will process the form parameters. Use the [body-parser middleware](https://www.npmjs.com/package/body-parser).

Here's an example: [Use ExpressJS to Get URL and POST Parameters: POST Parameters](https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters#post-parameters).
