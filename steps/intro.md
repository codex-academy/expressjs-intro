---
layout: default
---

# Intro

## Get going with Express JS

ExpressJS is a web server for NodeJS.

### Port numbers

When starting a ExpressJS server it binds a process to a port number on the server it's started on. Port numbers allow one to start multiple ExpressJS server instances on the same server, each one with it's own port number.

This example starts a server instance on port 3000:

```javascript
var express = require('express');
var app = express();

//start the server
var server = app.listen(3000);
```

This server instance is not useful, as it expose no routes.

### Routes

Routes can be accessed using the Http protocol. ExpressJS support all the Http request verbs. We will focus on POST and GET requests.

To add a route to our server instance.

Add some code before the `app.listen` method call.

```javascript
app.get('/hello', function(){
    req.send("Hello world!")
}};
```

Our server instance now have a `/hello` Http GET route.

### Install Express JS

Now run your own ExpressJS server locally.

* Create a new folder in your projects folder called `express-app`;
* change into this folder using `cd express-app`;
* type `npm init` accept all the defaults - this create a `package.json` file;
* install ExpressJS and save it as a dependency the package.json automatically by running `npm install --save express` . The `--save` parameter ensure the the dependency that is installed are stored in the `package.json` file.

 Read more details about [installing ExpressJS](http://expressjs.com/starter/installing.html) here.

### Basic Express server instance

Create a file called `server.js` and copy the text below into it:

```javascript
var express = require('express');
var app = express();

// create a route
app.get('/', function (req, res) {
 res.send('Hello World!');
});

//start the server
var server = app.listen(3000, function () {

 var host = server.address().address;
 var port = server.address().port;

 console.log('Example app listening at http://%s:%s', host, port);

});
```
**Now try this:**

* Start the server by typing `node server.js` and press enter in the console.
* In a web browser navigate to http://localhost:3000/
* Stop the server in the console by pressing Ctrl-C in the console a few times.
* Now navigate to http://localhost:3000/ again. What happens?
* Start the server and again.
* Try to navigate to `http://localhost:3000/hello` - what happens? How can we fix that?
* Try this:
    * Stop the web server.
    * Add a new route for `/hello` that renders 'Hello codeX!' to the screen.
    * Start the server.
    * Now try to navigate to `http://localhost:3000/hello` What happened?
