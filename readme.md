# Frontend Mentor - Single price grid component solution

This is a solution to the [Single price grid component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/single-price-grid-component-5ce41129d0ff452fec5abbbc). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See a hover state on desktop for the Sign Up call-to-action

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Frontend Mentor](https://www.frontendmentor.io/profile/purvjadh)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

One key challenge I encountered was applying `gap` between sections. Initially the articles were block-level elements, and `gap` has no effect on block containers. The fix was to switch the parent to `display: flex` (or `display: grid`), which unlocks the `gap` property.

```css
/* gap doesn't work on block elements */
.card {
  display: grid; /* now gap works */
  gap: 0.5rem;
}

article {
  display: flex;
  flex-direction: column;
  gap: 0.5rem; /* spacing between child paragraphs */
}
```

I also practised using CSS custom properties to keep colours consistent across the component:

```css
:root {
  --clr-bg-primary: hsl(179, 62%, 43%);
  --clr-bg-light: hsl(179, 62%, 60%);
  --clr-btn-primary: hsl(71, 73%, 54%);
  --clr-bg-neutral: hsl(204, 43%, 93%);
  --clr-para-neutral: hsl(218, 22%, 67%);
}
```

And built the two-column desktop layout using CSS Grid with `span`:

```css
@media (min-width: 40em) {
  .card {
    grid-template-columns: repeat(2, 1fr);
  }

  .community {
    grid-column: span 2; /* full-width top section */
  }
}
```

### Continued development

- Refining responsive breakpoints and fluid typography
- Exploring more advanced CSS Grid layouts
- Improving accessibility — adding proper `aria` attributes and focus styles to interactive elements like the Sign Up button

## Author

- Frontend Mentor - [@purvjadh](https://www.frontendmentor.io/profile/purvjadh)
- GitHub - [@purvjadh](https://github.com/purvjadh)