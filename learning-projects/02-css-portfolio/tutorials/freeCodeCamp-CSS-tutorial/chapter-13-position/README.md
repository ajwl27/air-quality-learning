### CSS Position - Notes

- Default position is `static`: Element follows normal document flow (in order)
- `relative`: Like static but can move with `top/right/bottom/left`. The element's original space stays reserved
- `absolute`: Floats freely, positions relative to nearest `position`ed parent
- `fixed`: Sticks to viewport, stays where it is on the screen even while scrolling
- `sticky`: Normal until scroll point, then sticks like `fixed`. won't scroll with non-fixed/sticky parent

Each positioned element (`relative/absolute/fixed/sticky`) can:
- Overlap other content
- Use z-index to control stacking order


- We can use position `absolute` with e.g. `left: -10000px` to remove it from the page
- For a persistent footer bar we could use `position: fixed` with a `width` of `100%`, but we could also use `position:sticky` with `bottom:0` to position it at the bottom
- If we have internal (same page) links, e.g. `<a href="#one">One</a> `, we can set `html { scroll-behavior: smooth; }` to smooth the transitions when clicking those links