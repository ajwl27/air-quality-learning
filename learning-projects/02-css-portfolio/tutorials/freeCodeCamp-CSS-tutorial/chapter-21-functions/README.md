### CSS Functions - Notes

- All CSS functions are listed on the [Mozilla Developer Network Page](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions)

- It can be useful to use `min` or `max` with a viewpoint-height based relative size for font size: e.g. `--FS: max(1rem, 3vh);`
- Even better would be to use `clamp`: `--FS: clamp(1.75rem, 3vh, 2.25rem);`, where `1.75rem` is the minimum size, `3vh` is the *ideal size* and `2.25rem` is the maximum size.

- It can be useful to use `filter` with links, e.g.:
  ```css
  a:hover, a:focus {
    filter: brightness(150%);
  }
  ```
  - You can also use `hue-rotate(180deg)` to get a complementary color