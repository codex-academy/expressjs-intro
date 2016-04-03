---
layout: default
---

## Server side variables

Express route callbacks always take two parameters req and res.

Those two variables are HttpRequest (req) and HttpResponse (res) respectively:


[Http Response](/steps/http_response.html)
[Http Request](/steps/http_request.html)

## HTML forms parameters

It reads the form data, prints it to the console and sends it to the template to be rendered back to the client.
This example is only reading one field, but you can read all the fields that are being sent from the form to the route.

**Note:*** For this example to work add the [body-parser middleware](https://www.npmjs.com/package/body-parser) to your ExpressJS instance.

Here's an example: [Use ExpressJS to Get URL and POST Parameters: POST Parameters](https://scotch.io/tutorials/use-expressjs-to-get-url-and-post-parameters#post-parameters).
