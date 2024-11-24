### CSS Animations - Notes

- we can use `transform:` with different functions:
  - `transform: translateX()` moves items left and right compared to their initial locations
  - `transform: translateY()` does the same up and down 
  - `transform: translate()` for shorthand does both (left then right)

  - `transform: rotateX()` rotates objects up and down (in 3D), so `90deg` causes the object to become invisible
  - `transform: rotateY()` does the same but left to right instead of top to bottom
  - `transform: rotateZ()` rotates clockwise (or anticlockwise with a negative number). `rotate` shorthand

  - `transform: scaleX()` scales only in the up/down axis
  - `transform: scaleY()` does the same but only in the left/right axis
  - shorthand `transform: scale` does X then Y

  - `transform: skewX()` skews left/right
  - `transform: skewY()` skews up/down
  - `transform: skew()` shorthand for both, skews X first then Y

  - [MDN link to transform](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)


- we can set up **transitions** to happen eg when the user hovers over an element:
  ```css
  div:hover {
    background-color: midnightblue;
    transition-property: background-color;
    transition-duration: 2s;
  }
  ```
  - we can delay the transition happening until after a `transition-delay`
  - we can use multiple transition effects, e.g.: `transition-property: background-color, transform;`
    - if we do that, we can set up different `transition-durations` for each effect, and different delays: `transition-duration: 2s, 3s;`
  - we can change the timing effect of the transition: e.g. `transition-timing-function: linear;` (default is `ease`)
- we can use the shorthand `transition`: `transition:all 2s linear 0.5s;`


- Assuming we have a class `.animate`, we can add animations using something like the following:
  ```css
  .animate {
    animation-name: slide;
    animation-duration: 5s;
    animation-timing-function: ease-in-out;
    animation-delay: 1s;
    animation-iteration-count: 5;
    animation-direction: alternate;
    animation-fill-mode: forwards;
  }

  @keyframes slide {
    0% {
      transform: translateX(0);
    }
    33% {
      transform: translateX(300px) rotate(180deg) ;
    }
    66% {
      transform: translateX(-300px) rotate(-180deg) ;
    }
    100% {
      transform: translateX(0);
      background-color: rebeccapurple;
    }
  }
  ```
  - in this example, we define an animation name, `slide`, and then we define `@keyframes` telling the browser what state the object will be in after defined percentages through the animation.
  - we give an `animation-duration` 
  - we define what timing function the animation should follow through the duration
  - we can define how many times the animation happens and in what direction the keyframes are followed
  - we can define an `animation-fill-mode` to change whether the object returns to its start mode or not at the end of an animation
  - shorthand compresses all of these onto one line: `animation: name duration timing-function delay iteration-count direction fill-mode;` e.g.:
  ```css
    /* animation-name: slide;
  animation-duration: 5s;
  animation-timing-function: ease-in-out;
  animation-delay: 1s;
  animation-iteration-count: 2;
  animation-direction: normal;
  animation-fill-mode: forwards; */
  animation: slide 5s ease-in-out 1s 2 normal forwards;
  ```
