# Frontend Mentor - Typing Speed Test solution

This is a solution to the [Typing Speed Test challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/typing-speed-test). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#the-link)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)



## Overview

This is challenge from Frontend Mentor to create a typing test where you can check your WPM and Accuracy along with other factors to push your limits. Have a great time going through!

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- Interactively be able to get their WPM and accuracy in different state factors

### Links

- Solution URL: [Add solution URL here]()
- Live Site URL: [Add live site URL here](https://anas-gh-000.github.io/Typing-test/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Vanilla JavaScript
- Json files


### What I learned

Learning new HTML properties, such as the options in the select tag, was new to me. While the concept was simple, it took me some time to fully grasp. Another major thing I learned was using Media Queries in CSS to make a site responsive. Trying to make this site responsive was my first attempt in this area. Although it was confusing at first, once I started working with it, it became comparatively easier to understand.

In the JavaScript part, there was a lot to learn. One of the major concepts was using localStorage and dividing a string’s characters to compare them with the user’s input. These concepts were initially unfamiliar and challenging to grasp. Since localStorage interacts more deeply with the DOM, and character division requires visually understanding the desired outcome, it took some effort. In this project, the goal was to compare user input to a given text and highlight each character as correct or incorrect.

The functions I wrote for WPM and accuracy calculations also required careful planning. I first had to create a logical flow of what I wanted to happen, then implement it in JavaScript, which was time-consuming. After writing the functions, debugging them and testing the start and disable functionality individually was also necessary.

```html
<select name="type-options" id="type-options">
  <option value="normal" selected>Normal</option>
  <option value="code">Coding</option>
</select>
```
```css
@media(max-width: 750px){}
```
```js
localStorage.setItem("personal_best_WPM", currentWPM);

function loadText(level){
    if (!typingData[level]){console.log(`Typing data not loaded yet; error.`); return;}     
    accuracyReset();
    wpmShowBox.innerText = 0;

    const passages = typingData[level];
    const randomIndx = Math.floor(Math.random()* passages.length);  
    const selectedPassage = passages[randomIndx];   
    let currentText = selectedPassage.text;   

    textDisplay.innerText = "";  
   
    currentText.split("").forEach(char =>{
        const span = document.createElement("span");
        span.innerText= char;
        textDisplay.appendChild(span);
    });

   
    typingInput.disabled = false;
    typingInput.value = "";
    typingInput.focus();
    
}
```

### Continued development

The areas I plan to focus on next are DOM manipulation and writing logical statements to create fully functional JavaScript functions. I also want to improve my use of semantic HTML, as well as continue refining site responsiveness using both CSS and JavaScript.

### Useful resources

- [W3 schools](https://www.w3schools.com/) - This website is essentially amazing for understanding JS details. Like how the localStorage works, and the Math() functions.
- [MDN documentation](https://developer.mozilla.org/en-US/) - I'd recommend this more for someone whose trying to dive deeper into CSS and semantic HTML. This really helped me in finding exact tags that would work for images and which values can help me modify it in CSS. Even the concept of flex display.

## Author

- Website - [Ana](https://anas-gh-000.github.io/Typing-test/)
- Frontend Mentor - [Ana](https://www.frontendmentor.io/profile/AnaS-gh-000)





