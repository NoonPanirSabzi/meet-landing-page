# Meet landing page

## Table of contents

- [Overview](#overview)
  - [Screenshot and live site URL](#screenshot-and-live-site-url)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Inspired by](#inspired-by)

## Overview

### Screenshot and live site URL

| Desktop                                     | Tablet                                    | Mobile                                    |
| ------------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| ![desktop](/assets/desktop-screenshot.jpeg) | ![Tablet](/assets/tablet-screenshot.jpeg) | ![Mobile](/assets/mobile-screenshot.jpeg) |

[Live Site URL](https://panir-meet.netlify.app/)

## My process

### Built with

- CSS Grid
- Responsive layout

### 🧠 What I Learned

Lots of valuable lessons! Here are the key ones:

1. **`100vw` includes the scrollbar in most browsers**  
   This can lead to layout shifts and headaches when aiming for pixel-perfect designs.  
   **Solution:** Prefer using `100%` or other layout strategies that don’t include the scrollbar width.

2. **Negative margins can pull elements in any direction**  
   Handy for overlapping or fine-tuning layout positioning.

3. **The CSS `transform` property**  
   Still working on mastering it.

4. **Positioning absolutely inside a relatively positioned container**  
   The theory made more sense once I used it in action.

5. **Centering an absolutely positioned element**  
   Shift the element 50% from the left of the container, then pull it back 50% of its own width:

   ```css
   .container {
     position: relative;
   }

   .child {
     position: absolute;
     left: 50%; /* this is 50% of the container width*/
     transform: translateX(-50%); /* this is 50% of the element width*/
   }
   ```

   🟰 Ta-da! Centered horizontally!  
   you can apply the same logic to the Y-axis for vertical centering.

6. **`z-index` only works on positioned elements**  
   That means `relative`, `absolute`, `fixed`, or `sticky`. It’s ignored if the element is `static`.

7. **Combining background image and color requires a `linear-gradient()`**  
   The color layer has to be a gradient—even if it’s just one color. otherwise it won't work ☹️

   ```css
   .element {
     background: linear-gradient(
         rgba(77, 150, 169, 0.8955),
         rgba(77, 150, 169, 0.8955)
       ), url("path/to/image.jpeg") center/cover no-repeat;
   }
   ```

8. **Flexbox vs. Grid**  
   If you need a managable two-dimensional layout, don't make my mistake of trying to build it with Flexbox  
   go with Grid from the beginning.

## Author

- Github - [@AminForouzan](https://github.com/AminForouzan)
- Frontend Mentor - [@AminForouzan](https://www.frontendmentor.io/profile/AminForouzan)

## Inspired by

- [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR).
