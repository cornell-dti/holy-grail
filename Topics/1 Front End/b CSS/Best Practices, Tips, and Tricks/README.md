# Avoid using `!important`
`!important` on any CSS rules forces that rule to take precedence over every
other rule, no matter what has previously been specified. The only way an
`!important` rule could be overridden is by another `!important` rule later
in the CSS file for the same element (or selector that targets the same
element.) [CSS specificity](https://designshack.net/articles/css/what-the-heck-is-css-specificity/)
details how an element should be styled with conflicting or overriding selectors.
Understanding the concept of specificity will make your CSS easier to understand,
and prevent you from ever needing `!important`.

# Don't use inline CSS styles
It's possible to put CSS styles directly on an HTML element, like this:

    <p style="color: red;">I'm red</p>

This makes our ultimate CSS for a paragraph tag unpredictable, for the same
reasons as using `!important`. Directly embedding CSS styles on an element
override any other styles that it is given (with the exception of an `!important`
rule.) It also creates a gap in what you intend to happen, and what actually
happens on a page. Keeping the content and styles of a page separate is
important to making everyone happy: You know where all the CSS is, you know
where all the HTML is, and the two don't mix.

# Reset CSS styles
All browsers have their say on what some CSS should look like. The "user
agent" of a browser, this can cause elements to behave differently across
browsing environments. As a developer, that becomes something of a headache
when your page looks just fine on one browser, but looks totally different
in another.

Use a [CSS Reset](https://necolas.github.io/normalize.css/) file, which
you should include *before any other CSS*, to make your intended and actual
CSS more consistent across environments. The above linked CSS reset also
fixes some common browser bugs or issues that may save you some stress further
in your web development adventures.

# Avoid Repetition
One of the CSS selectors is a comma, which allows you to chain multiple
selectors onto each other to apply the same rule(s). This can be helpful
to more logically structure your CSS file, and also group related CSS selectors
together.

# Further Reading
[This presentation](http://www.scottohara.me/htmlcss) goes over some of
the concepts mentioned here, in addition to other ideas like the Box Model,
custom fonts, adn more.