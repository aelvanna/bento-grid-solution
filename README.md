# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

**Desktop Preview**

![Desktop Preview](./desktop-preview.jpeg)

**Mobile Preview**

![Mobile Preview](./mobile-preview.jpeg)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/bento-grid-solution-mnTUdvgpLr](https://www.frontendmentor.io/solutions/bento-grid-solution-mnTUdvgpLr)
- Live Site URL: [https://bento-grid-solution-lf.netlify.app](https://bento-grid-solution-lf.netlify.app)

## My process

### Built with

- Semantic HTML5 markup
- BEM (Block, Element, Modifier)
- Fluid Typography
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- SASS

### What I learned

Through this project I improved my skills and knowledge on CSS.

I learned how to clip and position an image inside a card, without affecting the card height.

```css
.consistent-posting-card {
  /* Allows image to be clipped */
  overflow: clip;
  /*  Establish a positioning context for child elements. This makes the card
    the "anchor" for the absolutely positioned image inside it. */
  position: relative;

  &__image {
    /*  Take the image out of the normal document flow. This allows us to
        position it anywhere relative to its parent (the card). */
    position: absolute;
    /*  Move the image's bottom edge to be positioned below the card's bottom edge. */
    bottom: -2.2rem;
    width: 80%;
  }
}
```

The image of different social media platforms (illustration-multple-platforms.webp) had purple artefacts that appeared in the image transparency when added to its respective card. A filter was added to create subtle shadows that helped to mask these artefacts.

```css
 .multiple-accounts-img {
    /* Filter to add a very subtle shadow to help mask * /
    /* the faint purple edge artifacts on the image asset. */
      filter: drop-shadow(0 2px 8px hsl(0 0% 0% / 0.15));
      margin-bottom: $space-xs;
      max-width: 100%;
    }
```

I created a utility class to have headings that were hidden but accessible by screen readers for accessibility purposes. The key to this was the 'clip' and 'clip-path' properties.

```css
/*  Hides an element while keeping content accessible to screen
    readers */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  /* 'clip' is deprecated, use as fallback for older browsers, so for modern browsers use clip-path */
  clip: rect(0, 0, 0, 0);
  clip-path: inset(50%);
  white-space: nowrap;
  border-width: 0;
```

### Continued development

For future projects, I would like to continue improving my skills and knowledge of CSS and to utilise Javascript in my projects.

### Useful resources

[Responsively App](https://responsively.app) - Browser to check responsiveness of websites at different viewport sizes.

[CSS Grid Layout Guide](https://css-tricks.com/snippets/css/complete-guide-grid/) - Useful reference for setting up CSS grids and the properties associated with them.

[CSS Position: Relative vs Absolute](https://dev.to/neshaz/css-position-relative-vs-position-absolute-26ok) - Helpful resource explaining how the CSS property 'position' works.

[Inclusively Hidden](https://css-tricks.com/inclusively-hidden/) - Helped to provide a way to visually hide elements but keep them accessible to screen readers.

## Author

- Website - [Liza Fernandez](https://www.lizafernandez.dev)
- Frontend Mentor - [@aelvanna](https://www.frontendmentor.io/profile/aelvanna)
