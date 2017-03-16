---
layout: default
---

# View Engine

To make it easy to use Handlebars templates in ExpressJS we configure Handlebars as a view engine in ExpressJS. Using the [express-handlebars](https://www.npmjs.com/package/express-handlebars) module.

Configure it like this :

```javascript
app.engine('handlebars', exphbs({defaultLayout: 'main'}));
app.set('view engine', 'handlebars');
```

Then use it like this:

```javascript
var data_for_template = {};
res.render('template_name', data_for_template);
```
