### Notes
- Inline CSS (e.g. <p style="color:blue"> Example text</p>) is NOT good practice
- CSS is executed in order, with later CSS rules overriding earlier ones.
- Selectors with higher specificity (e.g. Class selectors vs element selectors) are executed with priority even if they're above the lower-specificity selector
- American english for CSS (color not colour). Problems such as misspelled CSS are *ignored*, and don't raise an error.
- To check for errors, you can use the [W3C CSS Validation service](https://jigsaw.w3.org/css-validator/#validate_by_upload)
- Selectors allow you to select all instances of that type
- Don't use ID selectors in CSS except in very rare circumstances as it's not best practice
- Class selectors (starts with . e.g. .gray) are the most common selectors
- Group selectors with a comma e.g.:
  h1, h2 {
    color: blue;
  }
- Select nested items without a comma e.g. for spans inside paragraph elements 
  p span {
    
  }
- Form elements typically don't inherit style
