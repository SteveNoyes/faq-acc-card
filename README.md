# Results summary component

## Table of contents

- [Overview](#overview)
- [Style Guide](#style-guide)
  - [Layout](#layout)
  - [Colors](#colors)
  - [Typography](#typography)
- [Screenshot](#screenshot)
- [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

## Screenshot

![Mobile](./assets/images/mobile.png)

![Desktop](./assets/images/desktop.png)

## Links

- Live Site URL: [Github Pages Hosting](https://stevenoyes.github.io/faq-acc-card/)

## My process
### Built with

- Mobile-first development
- Semantic HTML5
- CSS
- The smallest amount of JavaScript

### What I learned

```html
  <div class="img-wrapper">
    <!-- Mobile -->
    <img class="desk-icon mobile-toggle" src="./assets/images/illustration-woman-online-mobile.svg" alt="Aspect ration nightmare fuel">
    <img class="desk-icon-shadow mobile-toggle" src="./assets/images/bg-pattern-mobile.svg" alt="Aspect ration nightmare fuel shadow">
    <!-- Desktop -->
    <img class="desktop-desk-icon desktop-toggle" src="./assets/images/illustration-woman-online-desktop.svg" alt="Aspect ration nightmare fuel">
    <img class="desktop-desk-icon-shadow desktop-toggle" src="./assets/images/bg-pattern-desktop.svg" alt="Aspect ration nightmare fuel">
  </div>
```

```css
  .reverseIcon {
    transform: rotate(180deg);
  }
```

```js
  let acc = document.getElementsByClassName("accordion");
  for (let i = 0; i < acc.length; i++) {
    acc[i].addEventListener("click", function() {
      let reverseIcons = document.getElementsByClassName("verseIcon");
      let image = this.children[0];
      this.classList.toggle("active");
      image.classList.toggle("reverseIcon");
      let panel = this.nextElementSibling;
      if (panel.style.display === "block") {
        panel.style.display = "none";
      } else {
        panel.style.display = "block";
      }
    });
  }
```

### Useful resources

- [Mozilla Developers Network](https://developer.mozilla.org/en-US/) - Documenting for web technologies, including CSS, HTML, and JavaScript.
- [Transfonter](https://transfonter.org/) - Modern and simple css @font-face generator. TTF, OTF, WOFF, WOFF2 or SVG, 15 MB per file.
- [The Markdown Guide](https://markdownguide.org/) - If you want more help with writing markdown, I'd recommend checking out their site to learn more.

## Author

- Website - [Portfolio](https://stevenmnoyes.com)
- Github - [Github Profile](https://github.com/SteveNoyes/)
- LinkedIn - [LinkedIn Profile](https://www.linkedin.com/in/steven-noyes/)