### CSS Floats - Notes

- Floats were originally designed to wrap text around images, like in magazine layouts, but became widely used for creating multi-column layouts before modern layout methods like Flexbox and Grid
- When you float an element (using `float: left` or `float: right`), it's taken out of the normal document flow and shifted to the left or right until it **touches the edge of its container or another floated element**
- **Other elements will wrap around floated elements** - this is what creates the text-wrapping effect. However, container elements won't automatically expand to contain floated elements (known as collapsing)
- To prevent container collapse with floated elements, you have two main options:
 - Modern solution: Add `display: flow-root` to the container element, which creates a new block formatting context and cleanly contains all floated children
 - Traditional solution:  add `clear: both` to an element after the floats
- While floats are still supported and useful for their original text-wrapping purpose, modern layouts should generally use Flexbox or Grid instead, as they're more powerful and easier to maintain