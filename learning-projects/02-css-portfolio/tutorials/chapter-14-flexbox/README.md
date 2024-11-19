### Notes

- There's a [game for learning flexbox](https://flexboxfroggy.com/) 

- *Flexbox* is a layout model for arranging items in rows or columns
- Used for items that need to be spaced evenly
- Great for centering things (both vertically and horizontally)
- Helps make layouts that work across different screen sizes
- Better than methods like floats

**When making a container flex (`display: flex;`)**
- Child elements become 'flex items'
- Items line up in a row by default
- Items try to fit on one line
- Items can stretch to match the height of their siblings
- Items can grow or shrink to fill available space

### Basic Usage

Change flex direction:
- Make items go down instead of across with `flex-direction: column`
- Make items go across with `flex-direction: row` (default)
- Reverse either direction by adding `-reverse`

- Control item spacing:
  - Space between items using `gap: 20px`
  - Space out items horizontally with `justify-content`
    - `space-between`: Elements spread across container, first and last items touch edges
    - `space-around`: Elements get equal space around them (looks uneven because middle items share spaces)
    - `space-evenly`: All spaces are exactly equal - between elements and edges
  - Centre items with `justify-content: center`
  - Push items to end with `justify-content: flex-end`

- Control item alignment:
  - Centre items vertically with `align-items: center`
  - Stretch items to fill height with `align-items: stretch`
  - Put items at bottom with `align-items: flex-end`

- Control individual items:
  - Make an item grow to fill space with `flex-grow: 1`
  - Stop an item from shrinking with `flex-shrink: 0`
  - Set item's starting size with `flex-basis: 200px`
  - Shorthand for all three: `flex: 1 0 200px`

- Wrap items:
  - Make items wrap to next line with `flex-wrap: wrap`
  - Keep items on one line with `flex-wrap: nowrap` (default)

- Use shorthand for both `flex-direction` and `flex-wrap`: `flex-flow`.
  - e.g. `flex-flow: row wrap`

- `align-content` works like `justify-content` but for the vertical spacing between wrapped lines
  - `align-content: space-between`: Lines spread from top to bottom
  - `align-content: space-around`: Equal space around each line
  - `align-content: space-evenly`: Equal space everywhere
- Only works when you have `flex-wrap: wrap`
- Controls space **between lines**, while `align-items` controls items **within each line**

- Set items within a container to `display:flex` and you can centre any content within them (e.g. `justify-content: center; align-items:center`)

- `flex-basis` sets the initial size of items before remaining space is distributed
  - Use a value like `flex-basis: 200px` or `auto`
  - Items can grow/shrink from this size based on available space
  - Similar to min-width but more flexible

- `flex-grow` controls how items expand to fill extra space:
  - Default is 0 (don't grow)
  - `flex-grow: 1` means "take equal share of extra space"
  - Higher numbers take proportionally more space
  - Example: one item with `flex-grow: 2` takes twice as much extra space as items with `flex-grow: 1`

-The `flex` property combines grow, shrink and basis: `flex: 1 = flex: 1 1 0` (grow: 1, shrink: 1, basis: 0)

Common patterns:
- `flex: 1` to make items share space equally
- `flex: none` to prevent growing/shrinking
- `flex: auto` to size based on content then share remaining space