---
layout: default
---

# Middleware

One extends ExpressJS functionality using middleware.

We will look at middleware to:

    * process form variables;
    * to handle http sessions;
    * to display flash messages.

## Form Variables

To process variables sent from Http form posts add the [body-parser](https://www.npmjs.com/package/body-parser) middleware to ExpressJS.

This will enable the `req.body` variable in ExpressJS route handlers.

## Http Sessions

Storing state between Http calls.

Http is a stateless protocol, Http Sessions allow one to store variables between http calls.

To enable Http Sessions in ExpressJS one need to add some middleware. [express-session](https://www.npmjs.com/package/express-session)

## Flash messages

An easy way to display messages after a redirect.

[express-flash](https://www.npmjs.com/package/express-flash)
