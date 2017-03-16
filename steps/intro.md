---
layout: default
unitstandard: 115362-SO1-AC1
---

# Intro

## Get going with Express JS

[ExpressJS](expressjs.com) is a web server for NodeJS.

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

Routes can be accessed using the HTTP protocol. ExpressJS support all the HTTP request verbs. We will focus on POST and GET requests.

To add a `hello` route to the server add the code below before the `app.listen` method call.

```javascript
app.get('/hello', function(req, res){
    res.send("Hello world!")
}};
```

Our server instance now has a `/hello` HTTP GET route.

### Setup and run a ExpressJS server instance

Follow these steps to setup a ExpressJS server instance

* Create a new folder in your projects folder called `express-app`.
* Change into this folder using `cd express-app`.
* Type `npm init`. This will create a `package.json` file in the current directory, based on your answers to some questions.
  * `entry point` means the main file for your application. We're going to use `server.js`, so enter that.
  * `test command` for us is `mocha`. We'll use this feature of the `package.json` later, for automatic testing of our code.
  * `git repository` is the location of your repository, like `https://github.com/<username>/<repository>.git`. Since we're using GitHub to store our code, `npm` lets us use a shortcut like this: `<username>/<repository>`.
* Install ExpressJS and save it as a dependency in your `package.json` by running `npm install --save express`. The additional `--save` parameter makes `npm` add a line to your `package.json` file.

Read more details about [installing ExpressJS](http://expressjs.com/starter/installing.html) here.

### Basic Express server instance


Now create a file called `server.js` and copy the code below into it:

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
