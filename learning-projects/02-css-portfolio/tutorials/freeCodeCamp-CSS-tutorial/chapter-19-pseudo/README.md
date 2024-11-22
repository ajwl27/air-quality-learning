### CSS Pseudo - Notes

- Pseudo selectors include both pseudo classes as pseudo elements
- A pseudo class is a selector that selects elements that are in a specififc state
  - e.g. `a:visited`
  - A useful pseudo class is `:any-link`, which selects both the `link` and the `visited` pseudo classes
  - We can avoid having to repeat `nav` in `nav a:hover, nav a:visited` by using `is`: `nav :is(a:hover,a:focus)`
    - If we include a higher specificity element in an `:is()`, we increase specificity of the entire pseudo selector
    - A very similar selector to `is` is `where`, which works the same but **always has zero** specificity
  - Another useful pseudo class is `:target`, which selects the last page link selected (i.e. a `#` html link)

- We can base selectors on attributes, e.g. `.card img[alt]{}`
- We can select the opposite of a given pseudo selector using `not()` e.g. `.card img:not([alt]){}` (we could use something like this to check our page and make sure we've added alt attributes to images)

- A pseudo element is similar but they act like you've added a new html element into your document
  - Pseudo elements use two colons instead of the 1 used by pseudo classes
  - Examples include `::after`, `::before`, which allow us to style inline after or before an element
    - We could use `::before` and `::after` to add quotation marks to paragraphs:
      ```css
      .card p::before {
        content: open-quote;
      }

      .card p::after {
        content: close-quote;
      }
      ```
    - If you use the `::first-letter` pseudo element, it will apply to the `::before`, element if it exists