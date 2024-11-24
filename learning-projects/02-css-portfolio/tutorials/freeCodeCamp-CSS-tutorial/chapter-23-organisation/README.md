### Notes - CSS Organisation

- Follow how your team already does it 
- Use comments to make dividers in the css files
- Sort properties alphabetically
- In larger projects, follow a naming convention methodology, eg BEM - Block, Element, Modifier 
  - Modifiers are used for incremental style changes
  ```css
  /* || BLOCKS */
  /* aka components */
  .btn {
  width: 100px;
  height: 100px;
  border-radius: 15px;
  }

  /* || MODIFIERS */
  /* incremental style changes */

  /* Blocks with modifiers */
  .btn--secondary {
    background-color: yellow;
  }

  .btn--lean {
    transform: skewX(-10deg);
  }

  .btn--border-lg {
    border: 5px solid whitesmoke;
  }
  ```
  - Elements do not represent structure and have no standalone meaning
