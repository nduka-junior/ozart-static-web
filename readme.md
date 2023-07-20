# GSAP Scroll Trigger Documentation

This documentation explains the code provided in the HTML file and how GSAP (GreenSock Animation Platform) is used to create scroll-triggered animations. The code includes several animations for elements on the page, such as logo links, a hero section, social icons, and a portfolio section.

## Prerequisites
To use this code and interact with the animations, you need to include the GSAP library and ScrollTrigger plugin. You can do this by adding the following script tags in your HTML file:

```html
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://fonts.googleapis.com/css?family=Rubik" rel="stylesheet" />
<script src="https://cdn.jsdelivr.net/npm/gsap@3.12.2/dist/gsap.min.js"></script>
```

## HTML Structure
The HTML file contains various sections, each with different animations. The main sections are:

1. Navbar: A simple navigation bar with a logo and a menu button.
2. Hero Section: A section introducing "Sarah Jackson," a designer and creative director.
3. Logo Links: Social media icons displayed as logo links.
4. Learn More: A section with an image that appears with a scroll-triggered animation.
5. What I Do: A section showcasing different categories of services.
6. Portfolio: A section displaying images with a grid layout.

## GSAP Animations
The provided script section contains GSAP animations for different elements on the page. Here are the key animations:

1. Logo Links: The logo and menu icons in the navbar slide in with a bounce-in/out effect.
2. Hero Section: The text and image of "Sarah Jackson" slide in from different directions with a power-in/out effect.
3. Social Icons: Social media icons scale up when hovered over and slide in from the left with a back-in effect.
4. Learn More Image: The image in the "Learn More" section slides in from the left with a power-in/out effect when triggered by scrolling.
5. What I Do Cards: The cards in the "What I Do" section slide in from the left with a power-in/out effect.

## Scroll Trigger
GSAP's ScrollTrigger plugin is used to create animations based on scroll positions. For instance, the image in the "Learn More" section is animated when it enters the viewport, defined using the `scrollTrigger` option:

```javascript
gsap.from("#about_img", {
  duration: 1.3,
  x: -500,
  opacity: 0,
  ease: "power2.inOut",
  scrollTrigger: {
    trigger: ".learn", // Element to be animated
    start: "top 80%", // Start the animation when the top of the element is 80% inside the viewport
    end: "bottom 20%", // End the animation when the bottom of the element is 20% inside the viewport
    scrub: true, // Smoothly animate on scroll both up and down
    markers: true, // Optional: Add markers for debugging
  },
});
```

The `scrollTrigger` defines the trigger element, start, end, scrub, and markers properties for the animation.

## Note
Please make sure to have the required image and SVG files in the `static` folder or modify the file paths accordingly.

## Conclusion
This document explains the code and animations used in the HTML file, showcasing how GSAP and ScrollTrigger are utilized to create engaging and interactive scroll-triggered animations. For further information about GSAP or ScrollTrigger, you can visit the GreenSock website (https://greensock.com/).