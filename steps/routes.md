---
layout: default
---

# Routes

Routes is how an ExpressJS expose functionality. Routes can be added for all the different Http VERBS like POST, GET, PUT and DELETE. They can be accessed from Web Browsers or tool like [Postman](https://www.getpostman.com/).

## Static routes

One add routes like this:

```javascript
//this is a GET route
app.get('/hello', function(){

});

//this is a POST route
app.post('/hello', function(){

});
```

## Routes with parameters:

One can add routes to ExpressJS that contains parameters.

```javascript
app.get('/products/:id', function(req, res){
  console.log(req.params.id);
  res.send("you sent me : " + req.params.id);
});
```

This route will work for Http requests like:
`http://localhost:3000/products/77` and
`http://localhost:3000/products/007`

it will return:
    `you sent me : 77` and `you sent me : 007` to the browser.

This is very useful for creating edit or view pages in your web application where you can see or edit the details of a data entity. Using parameters (`req.params`) one can have on route that can take care of all edit/update actions.

Here's an example: [Use ExpressJS to Get URL and POST Parameters: Specific Routing for Specific Parameters](https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters#specific-routing-for-specific-parameters)

One can easily add routes like this:

```javascript

req.get('/urls/:param_one/url_part2/:param_two', function(req, res){
    //code goes here
});
```
