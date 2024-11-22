### CSS Units - Notes
- Mozilla have a list of [CSS values and units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
- The only absolute value often used is px (pixels)
- It's not good to use absolute font sizes, as accessibility features (font size options) on browsers won't rescale text with absolute (pixel) sizes
- Setting width to a percentage means it's set relative to the parent, e.g.: for this example,
in `index.html`:
```     <header>
        <h1>CSS Units</h1>
    </header>
```
in `style.css`:
```
header {
  width: 50%
}
h1 {
  border: 2px dashed red;
  width: 50%
}
```
The width of heading 1 is 50% of the 50% of the header width (25% of the `<body>`)
- The unit typically used for font size is the `rem`. This is a multiple of the default size for that element set by the browser (i.e. 2rem is twice as big)
- You can use `em` to set size equal to a multiple of the parent element
- We can do a *CSS reset* to override browser defaults, e.g.:
```
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}
```