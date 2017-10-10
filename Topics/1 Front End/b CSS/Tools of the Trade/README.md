# CSS Pre-Processors
CSS can get tricky. It has a lot of power and flexibility, but it can get
messy and complicated trying to maintain a CSS file. What if we could make
CSS extensible and easy to work with? Say, variables, functions, actual
nested elements, and more?

## LESS
### Syntax
```
.bordered {
  border-top: dotted 1px black;
  border-bottom: solid 2px black;
}
#header {
  color: black;
  .navigation {
    font-size: 12px;
  }
  .logo {
    width: 300px;
  }
}
#menu a {
  color: #111;
  .bordered;
}

.post a {
  color: red;
  .bordered;
}
```

### Works with
Node.js

### [Documentation](http://lesscss.org/features/)

## SASS (also known as SCSS)
### Syntax
```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```

### Works with
Node.js, Perl, Go, Ruby, C#, JavaScript, and Python

See [here](https://github.com/sass/libsass#excerpt-of-sanctioned-implementations)
for download links

### [Documentation](http://sass-lang.com/guide)

## Stylus
### Syntax
```
border-radius()
  -webkit-border-radius: arguments
  -moz-border-radius: arguments
  border-radius: arguments

body
  font: 12px Helvetica, Arial, sans-serif

a.button
  border-radius(5px)
 ```

### Works with
Node.js

### [Documentation](http://stylus-lang.com/)

All code samples taken from the developers' respective websites