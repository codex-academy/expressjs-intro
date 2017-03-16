---
layout: default
---

# Http Sessions

Storing state between Http calls.

Http is a stateless protocol, Http Sessions allow one to store variables between http calls.

To enable Http Sessions in ExpressJS one need to add the [express-session](https://www.npmjs.com/package/express-session) middleware to ExpressJS.

This will enable the `req.session` variable in ExpressJS route handlers.
