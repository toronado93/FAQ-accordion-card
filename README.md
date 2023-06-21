# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [My process](#my-process)
  - [What I learned](#what-i-learned)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

## ScreenShot

![Example Screenshot](/screenshot/image.png)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

### What I learned

I understand to usage of data-visible html attribute

      const buttons = document.querySelectorAll(".arrow_button");

      // Add click event listener to each button
      buttons.forEach((button) => {
        button.addEventListener("click", () => {
          // find h1 and toggle
          const h1 = button.previousElementSibling;

          if (h1.hasAttribute("data-visible")) {
            h1.setAttribute("aria-expanded", false);
            h1.toggleAttribute("data-visible");
          } else {
            h1.setAttribute("aria-expanded", true);
            h1.toggleAttribute("data-visible");
          }

          button.classList.toggle("rotate");
          const parentDiv = button.closest(".accordion_wrapper");
          const paragraph = parentDiv.querySelector(".accordion_sub_paragraph");
          paragraph.classList.toggle("show");
        });
      });

And I learned relationship between making repsonsive div
breakpoints and max-width usage

higher than breakpoint

main {
width: 100%;
max-width: 1440px;
/_ Add any other styles you need for the main element _/
}

Lower than breakpoint

.container {
width: 375px;
background-color: #ccc;
padding: 20px;
/_ Add any other styles you need for the container _/
}

Making image bigger than default size

.container {
width: 375px;
background-color: #ccc;
padding: 20px;
/_ Add any other styles you need for the container _/
}

Understanding how animation works

@keyframes fadeIn {
from {
opacity: 0;
}
to {
opacity: 1;
}
}

.accordion_sub_paragraph {
display: none;
}

.accordion_sub_paragraph.show {
animation: fadeIn 0.3s ease-in;
display: block;
}

Rotating Img,svg

.arrow_button {
transition: transform 0.3s ease-in-out;
}

.arrow_button.rotate {
transform: rotate(180deg);
}

      const buttons = document.querySelectorAll(".arrow_button");

      // Add click event listener to each button
      buttons.forEach((button) => {
        button.addEventListener("click", () => {
          // find h1 and toggle
          const h1 = button.previousElementSibling;

          if (h1.hasAttribute("data-visible")) {
            h1.setAttribute("aria-expanded", false);
            h1.toggleAttribute("data-visible");
          } else {
            h1.setAttribute("aria-expanded", true);
            h1.toggleAttribute("data-visible");
          }

          button.classList.toggle("rotate");
          const parentDiv = button.closest(".accordion_wrapper");
          const paragraph = parentDiv.querySelector(".accordion_sub_paragraph");
          paragraph.classList.toggle("show");
        });
      });
