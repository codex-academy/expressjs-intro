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

# Http Request

The HttpRequest object is about gathering input from the browser.

There are 3 ways to input data from the request object:

* URL paramaters using `req.params`;
* Query parameters using `req.query`;
* HTML forms parameters using `req.body`

### URL with parameters

Read more aboute routes with parameters [here](../steps/routes.html)

### Query paramaters

Query parameters can be sent into a route using a `?` after the route name.

For example a URL like:

`http://localhost:3000?name=Jo&last_name=Bloggs`

have query parameters that can be read like this:

```javascript

    var name = req.query.name;
    var last_name = req.query.last_name;

```

### req.body

To read parameters send from HTML forms one use the `req.body` paramater on the Http Request object sent into routes.

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

**Note:*** For this example to work add the [body-parser middleware](https://www.npmjs.com/package/body-parser) to your ExpressJS instance.

Here's an example: [Use ExpressJS to Get URL and POST Parameters: POST Parameters](https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters#post-parameters).
