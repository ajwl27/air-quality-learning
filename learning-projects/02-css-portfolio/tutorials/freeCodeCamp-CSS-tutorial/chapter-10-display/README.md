### CSS Display - Notes
- in the html file, the paragraphs are *block level elements*.
- block level elements stack on top of each other and always create a new line
- **block level elements** by default have 100% width (of their parent element, not necessarily of the whole viewport), and stack on top of each other
- a `span` element is an *inline level element*
- inline elements do not stack on top of each other and do not create a new line
- inline elements only take up the width of their content (unless we add extra left/right padding)
- we can't apply a top or bottom margin to (or change the height of)  an inline element
- we can if we change its `display: inline-block;` property though
- Changing list items `li {}` to `display: inline-block;` will put them into an inline row instead of a column of blocks