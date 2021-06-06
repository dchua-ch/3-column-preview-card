# Frontend Mentor - 3-column preview card component solution

Hi all, this is my second HTML/CSS project from [Frontend mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). 
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
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)



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

 I initially tried the following.

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
```js
const proudOfThisFunc = () => {
  console.log('🎉')
}
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
