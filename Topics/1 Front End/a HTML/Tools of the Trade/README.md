# HTML Pre-Processors
When working with a server-side language, it helps to be able to directly
embed data into a static HTML page. If you can avoid an excessive amount
of database transactions, why not go that route? HTML Pre-Processors allow
developers to directly embed data in HTML.

## EJS
### Syntax
```
<% if (user) { %>
  <h2><%= user.name %></h2>
<% } %>
```

### Works with
Node.js

### [GitHub](https://github.com/mde/ejs)

## FreeMarker
### Syntax
```
<h1>Welcome ${user}!</h1>
<p>Our latest product:
<a href="${latestProduct.url}">${latestProduct.name}</a>!
```

### Works with
Java

### [Documentation](http://freemarker.org/docs/index.html)

## Jinja2
### Syntax
```
{% for item in navigation %}
    <li><a href="{{ item.href }}">{{ item.caption }}</a></li>
{% endfor %}
 ```

### Works with
Flask (Python)

### [Documentation](http://jinja.pocoo.org/docs/2.9/templates/)

## Pug
### Syntax
```
ul
  each val in values
    li= val
  else
    li There are no values
```

### Works with
Node.js & Express

### [Documentation](https://pugjs.org/api/getting-started.html)

All code samples taken from the developers' respective websites