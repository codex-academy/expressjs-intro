---
layout: default
---

# Routes

Routes is how ExpressJS exposes functionality. Routes can be added for all the different HTTP VERBS like POST, GET, PUT and DELETE. They can be accessed from Web Browsers or a tool like [Postman](https://www.getpostman.com/).

## Static routes

You add routes like this:

```javascript
//this is a GET route
app.get('/hello', function(){

});

//this is a POST route
app.post('/hello', function(){

});
```

## Routes with parameters:

You can add routes to ExpressJS that contain parameters.

```javascript
app.get('/products/:id', function(req, res){
  console.log(req.params.id);
  res.send("you sent me: " + req.params.id);
});
```

This route will work for HTTP requests like:
`http://localhost:3000/products/77` and
`http://localhost:3000/products/007`

It will return `you sent me: 77` and `you sent me: 007` to the browser.

This is very useful for creating edit or view pages in your web application where you can see or edit the details of a data entity. Using parameters (`req.params`) you can have one route that can take care of all edit/update actions.

Here's an example: [Use ExpressJS to Get URL and POST Parameters: Specific Routing for Specific Parameters](https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters#specific-routing-for-specific-parameters).

You can add routes like this:

```javascript
req.get('/urls/:param_one/url_part2/:param_two', function(req, res){
    //code goes here
});
```
