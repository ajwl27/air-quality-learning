### CSS Styling Lists - Notes
- You can use shorthand to replace `list-style-image`, `list-style-type`, `list-style-position`: `list-style: square url("../images/checkmark.png") inside;`
- it's possible to use pseudoclasses to set only the nth item in a list: `ul li:nth-child(2) {color:red};` to set only the 2nd item red
- pseuo-*elements* can be used (e.g. `::marker {}`)