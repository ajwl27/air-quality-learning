### Notes

- Responsive design, especially to viewport width, is essential so the site looks good on different devices
- We add the meta tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">` to the html file to enable media queries and allow responsive design. *VSCode automatically adds that tag to html templates created with the `!` emmet abreviation*


##### Media query CSS syntax:

Syntax:
```css
@media media-type and (condition: breakpoint) {
    /* CSS rules */
}
```
Key points:
- the most common media type is `screen`
- We'd usually use `min-width` as the `condition` - that sets the minimum viewport width from which our CSS rules apply
- ##### It's important that we design our site for the `min-width` out to the max width rather than the other way around as that is the principle of *mobile-first design* 
  - It's easier to design this way as mobile design, as the hardest, should be done first. Once the mobile design questions are answered, designing for other devices will be easier
  - All styles above `@media` would be applied untl the screen width gets down to `breakpoint`, and then they would still be applied unless we were to overwrite them 

    Example:
      ```css
      /* Mobile styles (default) */
      .container { width: 100%; }

      /* Styles for 481px and above */
      @media screen and (min-width: 481px) {
          .container { width: 80%; }
      }
      ```

  - Mobile design us usually single-column
  

- Another `condition` we might want to use is `orientation`: `@media screen and (orientation: landscape){}`
- There's also `min-aspect-ratio`
- We can also combine more than one condition, e.g.: 
  ```css
  /* MOBILE DEVICE LANDSCAPE */
  @media screen and (max-height: 425px) and (min-aspect-ratio:7/4) {
    body {
      background-color: dodgerblue;
      background-image: radial-gradient(whitesmoke, dodgerblue);
    }
    h1, h2 {
      font-size: 1.5rem;
    }
    nav {display: none;}
  }
  ```


#### Common Media Query breakpoints:
| Breakpoint | Description |
| -------- | ---------- |
| < 481px | Mobile devices |
| 481px — 768px | iPads, Tablets |
| 769px — 1024px | Small screens, laptops |
| 1025px — 1200px | Desktops, large screens |
| 1201px and greater | Extra large screens, TV |

#### Tailwind breakpoints:
| Breakpoint | Description |
| -------- | ---------- |
| < 640px | xs |
| >=640px | small |
| >=768px | medium |
| >=1024px | large |
| >=1280px | xl |
| >=1536px | 2xl |

