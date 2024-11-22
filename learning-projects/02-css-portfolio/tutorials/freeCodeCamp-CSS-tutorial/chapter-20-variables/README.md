### CSS Variables - Notes

- Variables in CSS allow us to define things we want to use (e.g. Hexidecimal colour codes)
- variables go in the `:root` selector and start with `--`, e.g.:
  ```css
  /* || VARIABLES */
  :root {
    /* COLOR */
    --BGCOLOR: #85ffbd;
  }
  ```

- To apply a variable in the rest of the code, we use the function `var`:
  ```css
  background-color: var(--BGCOLOR);
  ```

- We can reference variables in other variables, e.g.: `--SHADOWS: 0 6px 5px -5px var(--DARK-COLOR);`

- If we set elements to multiple classes, e.g.: `<div class="square square--highlight"></div>`, we can set a rule for one class and redefine variables for elements of the additional class, without having to set the actual style again. 

  For instance, in the below example, all `square` class elements will have a `red` background colour apart from those that additionally have the `square--highlight` class.

  ```css
  :root {
    --SQUARE-BGCOLOR: red;
  }

  .square--highlight {
    --SQUARE-BGCOLOR: blue;
  }

  .square {
    background-color: var(--SQUARE-BGCOLOR);
  }

  ```
- You can set a different set of colours for dark mode, overriding colours we have already defined:
  ```css
  @media (prefers-color-scheme:dark){
    :root {
      --BGCOLOR: #000;
      --ALT-BGCOLOR: #333;
              ...
    }
  }
  ```