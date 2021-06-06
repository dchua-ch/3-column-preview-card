# Frontend Mentor - 3-column preview card component solution

Hi all, this is my second HTML/CSS project from [Frontend mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). You can check out the project [here](https://dchua-ch.github.io/3-column-preview-card/). I've also detailed my process and learning journey below. Any feedback is welcome!
## Table of contents

- [Frontend Mentor - 3-column preview card component solution](#frontend-mentor---3-column-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
      - [1. Button alignment using absolute positioning](#1-button-alignment-using-absolute-positioning)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)



## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot
*Mobile layout of 3 column preview card* 

![Mobile 3 column preview card](/images/3column_mobile_solution.png) 
 


*Desktop layout of 3 column preview card*
![Desktop 3 column preview card](/images/3column_desktop_solution.png)





### Links
- Live Site URL: (https://dchua-ch.github.io/3-column-preview-card/)

## My process

### Built with

This project was built using a mobile-first workflow and CSS Flexbox. I completed the CSS styling for the mobile layout first before using a media query to construct the desktop layout.

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

This project helped me to practice my CSS Flexbox skills. In particular, I had some trouble with positioning the "Learn More" button. I highlight one of the challenges I faced while completing this project below.

#### 1. Button alignment using absolute positioning
 
 I found that, in desktop mode, the buttons may lose their horizontal alignment with each other when the viewport is resized by the user. This is shown in the screenshot below.

![Screenshot of solution with buttons misaligned](/images/uneven_buttons.png) 

*Screenshot of solution with misaligned buttons in desktop mode* 
 
 To fix this problem, I set my button elements to position: absolute and the "text-container" class to position: relative. The text-container class is set to the three divs containing the three columns. This would allow me to set the position of the buttons relative to the text-container divs.

 I initially tried setting bottom: 0; to the button elements. However, this shifted the buttons to the bottom border of the text-container divs. That is, the button positioning ignored the padding of the text-container divs. To solve this problem, I defined a CSS custom property called "--text-container-padding". I then set padding-bottom of the text-container div to 2 * var(--text-container-padding) and bottom of the button to var(--text-container padding). This fixed the vertical position of the buttons while providing the desired padding on the bottom of the text-container div.

```css
.text-container {
    padding: var(--text-container-padding);
    /* add additional padding to account for button */
    padding-bottom: calc(var(--text-container-padding)*2);
    /* to make button positioning relative to .text-container */
    position: relative;   
}


button {
    background-color: var(--headings-buttons-color); 
    border-radius: 1rem; 
    /* adding border:0; gives buttons a flat look */
    border: 0;
    height: 2rem;
    width : 6rem;

    /* set position absolute and shift button to 1 padding above bottom of 
    .text-container div. This will fix button's position when screen is resized.
    Without this, unequal paragraph heights would affect button position */
    position:absolute;
    bottom: var(--text-container-padding);
}
```
With the above code, the buttons would maintain their horizontal alignment with each other when the user resizes the viewport. You can refer to the solution screenshots :D. 

### Continued development

In future projects, I would like develop the following skills.

1. DOM manipulation with JavaScript
2. CSS Grid
3. Designing my own projects using software like Figma or Adobe XD and then implementing them in HTML/CSS/JavaScript


### Useful resources

- [flex-cheatsheet](https://yoksel.github.io/flex-cheatsheet/) A cheatsheet for CSS FlexBox which I referred to. 
- [MDN Web Docs](https://developer.mozilla.org/en-US/) General HTML and CSS reference. Highly useful.


