# Include `<!DOCTYPE html>` at the top of every HTML page
`<!DOCTYPE html>` tells a browser what version of HTML this page is written
in. You may have heard of HTML5, or just plain HTML. The current standard,
HTML5, is what all HTML pages should be written in.

HTML5 is not another way of writing HTML; rather, it's not another language
or functionally different form of HTML (not like going from Python 2 to 3).
Instead, HTML5 builds upon the previous version of the standard so much
so that it becomes necessary to refer to it in a different way than its
predecessor.

`<!DOCTYPE html>` says to a browser that this page is written specifically
in HTML5. Quoting the [HTML5 Specification](http://w3c.github.io/html/syntax.html#the-doctype):

> 8.1.1 The DOCTYPE

  > A DOCTYPE is a required preamble.

  >
  DOCTYPEs are required for legacy reasons. When omitted, browsers tend
  to use a different rendering mode that is incompatible with some specifications.
  Including the DOCTYPE in a document ensures that the browser makes a best-effort
  attempt at following the relevant specifications.

# Include `<meta charset="UTF-8">` in your `<head>`
`<meta charset="UTF-8">` informs the browser of the character encoding
of this page. Rather than being simply plain text, it follows Unicode
Transformation Format 8, allowing a wide variety of characters and languages
to be displayed on screen.

# Change the viewport
    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
This line, when put in the `<head>` instructs the browser to do the following
(based on the comma-separated list of instructions in the `content` attribute
of that line):

* Set the width of the current page to follow the screen width of the current
device. This width will vary depending on the device currently being used
(computer, tablet, phone)

* Reset the zoom level of the page to be equal to 1.0, whereas a page
might have been zoomed in or out in the past.

# Use other `<meta>` tags to your advantage
    <meta name="author"      content="Shea Belsky">
    <meta name="description" content="The Holy Grail for Cornell DTI and the web community">
    <meta name="keywords"    content="DTI, Cornell DTI, Design and Technology Initiative">

# Do not use the `style` attribute on any element
Using `style` is bad practice, and can directly conflict with CSS that you've
previously instructed an element to have. It's also hard to keep track of
such CSS, since it's never in a CSS file. Only use CSS from selectors and
rules to give an element some styling.

# Further Reading
https://github.com/hail2u/html-best-practices