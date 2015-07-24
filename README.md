# The CSS Code Review Checklist

The ultimate code review guide and checklist on CSS.

These are compiled based on my experiences, observations, best practices I have been a part of. Besides serving these as a self guide, I am offering this as a suggestive checklist on code reviewing JavaScript. Hope this helps you.

This will be a work in progress since code review is an art and you just cannot hava a checklist that is long enough.

Go To
* [Plain o' CSS](#plain-O'-css)
* [SASS](#sass)
* [LESS](#less)

## Plain O' CSS

### Formatting
* Create Mixins if you think this style can be reused.
* Use hyphens when naming mixins, extends, classes, functions & variables: `span-columns` not `span_columns` or `spanColumns`.
* Use space between property and value: `width: 20px` not `width:20px`.
* Use a blank line above selector that has styles.
* Prefer hex color codes `#000`.
* Use `//` for comment blocks not `/* */`.
* Use a space between selector and `{`.
* Use double quotation marks.
* Use only lowercase, including colors.
* Don't add a unit specification after `0` values, unless required by a mixin.
* Use space around operands: `$variable * 1.5`, not `$variable*1.5`
* Avoid in-line operations in shorthand declarations (Ex. `padding: $variable * 1.5 variable * 2`)
* Use parentheses around individual operations in shorthand declarations: `padding: ($variable * 1.5) ($variable * 2)`

### CSS Order
* Use alphabetical order for declarations.
* Declarations with directions (`border-top`, `border-right`) should be grouped clock-wise from `top`.
* `top`, `right`, `bottom`, `left` should be grouped after the alphabetized list.
* Place @extends and @includes at the top of your declaration list.
* Place media queries directly after the declaration list.
* Place concatenated selectors second.
* Place pseudo states and elements third.
* Place nested selectors last.

### CSS Selectors
* Avoid using ID's for style.
* Use meaningful names: `$visual-grid-color` not `$color` or `$vslgrd-clr`.
* Use ID and class names that are as short as possible but as long as necessary.
* Avoid using the direct descendant selector `>`.
* Avoid nesting more than 4 selectors deep.
* Don't nest more than 6 selectors deep.
* Use HTML tags on vague classes that need a qualifier like `header.application` not `.main`.
* Avoid using the HTML tag in the class name: `section.news` not `section.news-section`.
* Avoid using HTML tags on classes for generic markup `<div>`, `<span>`: `.widgets` not `div.widgets`.
* Avoid using HTML tags on classes with specific class names like `.featured-articles`.
* Avoid using comma delimited selectors.
* Avoid nesting within a media query.

## SASS

Deferring to [Sass guidelines](http://sass-guidelin.es/)

## LESS

Most of the general CSS guifklines appy here. But again
* Take a look at _Less standards_ in [LESS Docs](https://github.com/less/less-docs)
* Create mixins to enable DRY culture
* Name classes based on one of these scenarios -
   - Functional (what the element does)
   - Content (what element contains)
   - Presentational (hows does element appear)
