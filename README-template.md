# Frontend Mentor - Social links profile solution

This is my solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). The goal was to build a small profile card with an avatar, a name, a location, a short bio, and a list of five social links, matching the provided design.

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

- See hover and focus states for all interactive elements on the page
- Navigate the social links with a keyboard (Tab / Shift+Tab)
- View the card comfortably on both mobile and desktop screens

### Screenshot

![](./screenshot.png)

*Screenshot of my finished solution.*

### Links

- Solution URL: [github.com/jkwiafe/Frontend-Mentors_Social-links-profile](https://github.com/jkwiafe/Frontend-Mentors_Social-links-profile)
- Live Site URL (Netlify): [frontendmentorssociallinksprofile.netlify.app](https://frontendmentorssociallinksprofile.netlify.app)
- Mirror (GitHub Pages): [jkwiafe.github.io/Frontend-Mentors_Social-links-profile](https://jkwiafe.github.io/Frontend-Mentors_Social-links-profile/)

## My process

### Built with

- Semantic HTML5 markup (`<header>`, `<ul>`/`<li>`, `<a>`)
- Plain CSS (no frameworks, no build step)
- Flexbox for centering the card and stacking the links
- `:hover` transitions for the interactive link rows
- Mobile-first sizing

### What I learned

- **Semantic list markup for links.** Using a real `<ul>` for the social links (instead of a stack of divs) means screen readers announce "list, 5 items" and users can navigate them together.
- **Flexbox centering.** I used `display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh;` on the body to center the card. I now know `min-height: 100vh` is safer because content won't get clipped on short viewports.
- **Hover vs focus.** My hover state (green background + slight scale) works well for mouse users. I learned the hard way that keyboard users get *no* feedback because I styled `li:hover` rather than `a:focus-visible` — that's my top fix for next time.

### Continued development

I'm still getting comfortable with Flexbox — specifically the difference between `flex`, `flex-grow`, `flex-basis`, and when to use `align-items` vs `align-content`. Concrete next steps:

- Move the hover styles onto the `<a>` itself so `:focus-visible` gives keyboard users the same feedback as mouse users.
- Replace the `<h3>` location line with a `<p>` and set the avatar's `alt` to `""` (the name is already in text next to it).
- Swap `height: 100vh` for `min-height: 100vh` and take the attribution out of `position: absolute` so it can't overlap the card.
- Refactor the theme colors into CSS custom properties on `:root` so I can tweak them in one place.
- Add a `prefers-reduced-motion` guard around the transitions.

### Useful resources

- [A Complete Guide to Flexbox – CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) – my reference whenever `align-items` and `justify-content` get confusing.
- [MDN – `:has()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:has) – useful for styling a parent row when its link is focused.

## Author

- Frontend Mentor - [@jkwiafe](https://www.frontendmentor.io/profile/jkwiafe)
- Instagram - [@jkwiafe](https://www.instagram.com/jk.wiafe)
