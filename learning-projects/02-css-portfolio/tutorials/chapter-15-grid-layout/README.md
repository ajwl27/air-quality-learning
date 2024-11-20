### Notes

- Core Concepts:
  - Two-dimensional layout system (handles rows and columns simultaneously)
  - Container becomes grid with `display: grid`
  - Define columns using `grid-template-columns`; rows with `grid-template-rows` (there's also `grid-auto-flow`)
  -  `gap` creates spacing between elements: ` gap: 0px 100px;` creates 100px gap on columns, 0px gap on rows

- Column Definition:
  - Fixed widths: `grid-template-columns: 200px 100px 200px` creates exactly that - three columns of those widths
  - Fractional units (`fr`) divide available space: 
      - `grid-template-columns: 1fr 1fr 1fr` splits space into three equal parts
      - `grid-template-columns: 2fr 1fr 1fr` first column takes 1/2 of space, others each take 1/4
      - Shorthand: `grid-template-columns: repeat(3, 1fr)` creates three equal columns
  - Mix units: `grid-template-columns: 200px 1fr 1fr` creates fixed first column, remaining space split equally

- Items can span multiple tracks: `grid-column: span 2` on the element

- Item Positioning:
  - Change the rows and columns occupied by an item: `grid-row-start`, `grid-row-end`, `grid-column-start` `grid-column-end`
  - Or use shorthand:
    - Line-based placement: `grid-row: 1 / 3`
    - Negative indices target from end: `grid-column: 1 / -1`
  - Named grid areas for semantic layouts
  - Can also use `grid-area` as shorthand for both `grid-row` and `grid-column`: `grid-area: 1 / 1 / 3 / 6;` sets `grid-row-start:1`, `grid-row-end:1`, `grid-column-start:3` and `grid-column-end:6`

- Tracks & Gaps:
  - Row definition: `grid-template-rows`
  - Gap syntax: `row-gap`/`column-gap` or `gap` shorthand
  - Dynamic rows: `grid-auto-rows`: you can use `grid-auto-rows: minmax(100px, auto)` so that rows are a minimum of 100px but automatically expand to the height of the container

- We can nest a grid inside a grid item

- Alignment:
  - `justify-items`/`align-items`: center/start/end
  - `place-items` shorthand for both axes
  - `justify-content`/`align-content` for grid container

- Rather than using auto grid or setting the span of items manually we can use *grid template areas*.
- Template Areas:
  ```css
  grid-template-areas:
      "header header"
      "sidebar main"
      "footer footer"
  ```
(Must maintain consistent column count per row)


- Viewport units combine well with Grid for full-page layouts
- practice game at [CSS Grid Garden](http://cssgridgarden.com/)