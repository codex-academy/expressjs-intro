---
layout: default
---
# Static files

One can configure ExpressJS to display content from static files. This is useful for client side scripts and css files.

Read how to do that [here](http://expressjs.com/starter/static-files.html).

Let's go ahead:

* and add a public folder in your spaza-app folder
* change your server.js file to render static files from the public folder using this, `app.use(express.static('public'));`
* in the public folder create a file called index.html and add some content to it
* Navigate to the file using http://localhost:3000/index.html
* If you are using nodemon no server restart would be required. If not, restart your server (please start using nodemon!).
* Going forward you will be able to use the public folder to store and reference css files and images from.
