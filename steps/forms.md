# Capture and storing data

So far you have spent a lot of time and effort slicing and dicing data. You started off using a CSV file as a data source which you then migrated into a database. Once your data was in the database it became much easier to query that data. How do we get data into your database? That is what we will explore next. We will go one step further, we will start capturing data from a web browser and storing it in a database.

To capture data on a web page one needs an HTML form with fields to allow data to be entered into the web page. Once the data is entered on the web page one needs to store the data somewhere. There are various different ways of doing that, but we will be focusing on web forms.

## Web forms

The `<form>` element wraps the various different types of web form elements.

The basic web form elements used for capturing data are:
* input - various different types including:
    * text
    * button
    * radio
    * checkbox
* text area
* button
* submit
* select
* hidden

A web form needs action and type attributes and a submit button.

For example:

```html
  <form action="/add_product" type="POST">
    Product name: <input type="text" name="product_name">
    <input type="submit">
  </form>
```

The web form above will send a `POST` request to the `add_product` route. The form will contain the value that was entered in the browser in the `product_name` field of the form.

You can use CSS to style your HTML forms. They can be tricky to style.
