---
layout: default
---

# Http Request

The HttpRequest object is about gathering input from the browser.

There are 3 ways to input data from the request object:

* URL paramaters using `req.params`;
* Query parameters using `req.query`;
* HTML forms parameters using `req.body`

### URL with parameters

Read about routes with parameters [here](../steps/routes.html)

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

### req.body

To read parameters sent from HTML forms to the server you use the `body` attribute on the HttpRequest object sent into routes.

For a html form that looks like this in html:

```html
<form action="/add_product" method="POST">
    Product name : <input type="text" name="product_name" >
    <input type="submit">
</form>
```

The `product_name` form parameter will be available on the server side in the `req.body` attribute in a route setup like this:

```javascript
app.post('/add_product', function(req, res){
 var formData = req.body;
 console.log(formData.product_name);
 res.render('product', {product_name :  formData.product_name});
});
```

