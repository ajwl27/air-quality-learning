### CSS Styling Links - Notes
- You can remove underlines from links with `text-decoration: none;`
- You can define a *pseudoclass* style with a colon; i.e. for the class for links `a : {}`, the pseudoclass for visited links would be `a:visited{}`
- We should use `a:focus` as well as `a:hover` (often in the same style) as `focus` is important for screenreader accessibility
- We still need to consider specificity and the order the styles are in the cascade; if `a:visited` is above `a`, `a:visited`'s properties will remain set even if `a` would override them
- - This is even more important for `a:hover` and `a:visited` as hover styles won't work on visited links if `a:hover` is above `a:visited` in the stylesheet
- - Usual order would be `a`, `a:visited`, `a:hover, a:focus`, `a:active`