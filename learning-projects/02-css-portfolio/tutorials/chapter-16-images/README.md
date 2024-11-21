### Notes

#### Image basics
- Images are not block-level elements- they are inline elements.
  - This can be changed by a img-specific css reset; `img {display:block;}`
  - When inline, images by default have a bit of bottom margin which might not be wanted. This is removed when set to display as a block element
  
- When styling an image, `width` and `height` percentages refer to not the image size but the container size.
  - Setting the `width` or `height` to a percentage allows the image to become responsive to the viewport size
  - We can set a `min-width` to prevent the image being below a set size
- You need to set `height:auto` if you set a `width` and want the image to scale evenly, and vice-versa

#### `<figure>`
- If we put an image into a `<figure>`, as we should, we style the image by:
  - Styling the class of the `figure` `.examplefigure{}` to `width:10%`
  - Styling the subclass: `.examplefigure img {width:100%; height: auto}`

- We should use a `<figcaption>` for accessibility, but can hide it from the page:
  
  ```
  .offscreen {
    position: absolute;
    left: -10000px;
  }
  ```

- We can circularise a square image: `border-radius:50%;`

#### Background Images
- We can set `background-image` to a file using `url`
- Control background tiling with `background-repeat`
- For big background images, you can use `background-size: cover;` to see the whole image
- Use `background-position:` to change the part of the image seen (if we're cropping an image bigger than the container)


#### Misc
- Add text shadow with `text-shadow: 2px 2px 5px #000;` - x axis, y axis, blur value, colour
- Create gradient backgrounds with `background-image:linear-gradient(colour 1, colour 2)`. 
  - You can add as many colours as desired i.e. `background-image:linear-gradient(colour 1, colour 2, colour 3, colour 4)`
  - You can change the gradient direction: `background-image:linear-gradient(to left, colour 1, colour 2)`
  - You can have both a gradient background and an image background, e.g. `background-image:url("../img/bubbles.png"), linear-gradient(to left, steelblue, white)`
    - If we do that we can scale each background component: `background-size:20%, auto;` sets background image to 20%, gradient to auto (same order as it was defined in background-image)
- You can clip a background image to text:
  ```
  background-image: url("../img/scenic-2200x1331.png");
  background-size: 100%;
  -webkit-background-clip: text;
  color: transparent;
  ```
  - If doing so we should use both `background-clip` and `-webkit-background-clip` for browser compatability