# CSS: What is it?
*CSS*, short for **C**ascading **S**tyle**s**heets, is the driving force
behind a website's visuals and design. Without CSS, we would not be gifted
with amazing things like [this cool submarine](https://codepen.io/ajerez/pen/EaEEOW),
[Cornell's own class roster](http://classes.cornell.edu), or [this adorable cat](https://codepen.io/bysusanlin/pen/epxBOV).

How does it all happen?

CSS declares the styling and visual elements of our site, and can also
change the structure and organization of a website. Styles in CSS files
override inherent styles in the browser (hence why they cascade over what
a browser says something should look like.)

# CSS: Setting it up
All files that use CSS will have this line of code:

`<link rel="stylesheet" type="text/css" href="css/stylesheet.css" >`

`rel` – Specifies the relationship between the page and the linked file; argument of "stylesheet" says that the linked file is a stylesheet.

`type` – Specifies the type of file; "text/css" tells us the linked file is encoded as a text file and structured as CSS

`href` – Specifies where (in relation to the current file) the file we want to link to is. Normally in a "css" or "styles" folder.

Goes in `<head>` of HTML document only!

# CSS: Syntax
ID: This will have the attributes described in the id named `one`.
IDs are represented with a pound symbol (`#`).
```
#one {
  text-align: center;
  color: red;
}
```
CLASS: This will have the attributes described in class named `center`
Classes are represented with a period (`.`).
```
.center {
  text-align: left;
  color: blue;
}
```

# CSS: Classes and IDs
IDs are unique: Each element can only have one ID, and each page can only
have one element with that ID. Use this for navigation containers, general
content wrappers, or unique elements on pages that do not repeat.

```
<div id="nav"></div>
```

Classes are not unique: You can use the same class on multiple elements,
and you can use multiple classes on the same element. Use this for navigation
list elements, repeated content divs, and images with identical styling.
```
<div class="nav-item"></div>
<div class="nav-item active"></div>
```
Elements CAN have both an ID and a class.
```
<div id="circle" class="html"></div>
```

# CSS: Selectors
We can select all of a given element, either across our site or as a child
of a given element, to apply CSS to it. Any HTML tag works.

`a` – Selects all links (a tags)

`img` – Selects all images (img tags)

`nav` – Selects all navigation menus (nav tags) (HTML5 element)

`html` – Selects the entire HTML page (these will not "cascade" to all elements,
it will just apply a certain style to the page but not its children.
Use `*` for global styling)

`body` – Selects the entire body of your HTML.

`.class1` – Selects a class named "class1"

`#id2` – Selects an id named "id2"

# CSS: Selectors
If we want to select special elements that lack a class or id, or are otherwise
difficult to style with CSS, the following syntax will help.

`elementA + elementB` – Selects any elementB that is a sibling or neighbor
of `elementA`

`elementA ~ elementB` – Selects any `elementB` that is preceded by `elementA`
(only works with preceded elements, see above for successive)

`.class1 .class2` – Selects all `class2` elements that are children (direct
or distant) of `class1`

`elementA > elementB` – Selects all `elementB` that are direct children of
`elementA`

`elementA.classB` – Selects all `elementA` elements that have a class of `classB`
as well

`elementA#idB` – Selects all `elementA` elements that have an ID of `idB` as well

`elementB *` - Selects everything that is a child (direct or distant) of
`elementB`. Use with caution.

`#id1, #id2` – Select `id1` and `id2`.

# CSS: Common Rules
Instructions in CSS are known as rules; they are commands by CSS that HTML
elements should follow. Some common CSS rules are listed below.

`color` - Change the color of text. RGB, hexadecimal, color name

`text-align` - Changes alignment of text. `left`, `center`, `right`

`font-family` - Changes font of text. "Web safe", custom, Google Fonts

`font-size` - Changes font size. Pixel, percentage, em units.
 
`text-transform` - Changes capitalization of text. `uppercase`, `capitalize`, `lowercase`

`text-shadow` - Changes shadow behind text. `[x]px [y]px color`

`line-height` - Changes line-height of text. Pixel, percentage, em units.

`height` – Changes height of image. Pixel, percentage, em units

`width` – Changes width of image. Pixel, percentage, em units

`background-image` – If you want to give your site a background image.
You would not need to use an img tag for this, just make sure your site
has the appropriate CSS class, ID, or element name.

`float` – Force an image to the `left` or `right`.

`display: block; margin: 0 auto` – Centers your image horizontally.
Two different lines, just written on one here because they need to go together
or it won’t work

# CSS: Percentages
When using percentages with CSS, the percentage dictated will tell the element
to adjust its size based on its parent.

`height: 100%;` on an image says to take up 100% the height of its parent

`width: 50%;` on a div says to take up 50% of the width of its parent

If the parent has no specified height or width, the percentage of its child
will resize based on its grandparents until it reaches the highest element
to determine a size.

Percentages can be used with `margin`, `padding`, `left`/`right`/`top`/`bottom`
among other things. Use with caution, it might not always do what you expect.

# CSS: Centering Things
Horizontal centering:

* Text: use `text-align: center;` to center text within an element
* Images & everything else: use `display: block;` and `margin: 0 auto;`

Vertical centering:
* Text: `line-height` and `height` for a text element should be the same
* Images:  Same as above, but you must add `vertical-align: middle;`

Horizontal AND Vertical centering:
* `display: flex; justify-content: center; align-items: center;`
