### Notes
- We can make a `<section>` and give its class the style `column-count: 4;`
- By default, the columns won't be limited to 1 paragraph per column - content will spread across columns according to viewport size
- If we define a `column-width` property, the columns will never be smaller than that value. Therefore if the viewport is too small, some columns will not be created
- We can use the shorthand `columns` to define number and width in one go: `columns 4 250px;`
- If we set the top margin of `p` elements inside a column to 0, we can ensure there's no weird space at the top of the first column. Due to **marign collapsing**, this won't actually change the spacing between paragraphs; the top and bottom margins are collapsed so that the bigger one is the margin (so with top margin set to 0 and bottom margin untouched, the bottom margin dictates spacing)
- We can use `break-inside: avoid;` to stop elements being split across multiple columns
- We can use `column-span:all;` to make an element spread across all columns
- we can stop a `span` of text being split onto multiple lines when resizing the viewport by using the `text-wrap:nowrap;` or `white-space: nowrap;` style