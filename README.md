# Website Performance Optimization 

## How to Run
1. Clone the repository or download the zip file
2. Open `index.html` in your browser

## Optimize PageSpeed Insights score for index.html

For this project, I optimized Cameron Pittman's portfolio website. First I tested this site on Google PageSpeed Insights (https://developers.google.com/speed/pagespeed/). This website scored 28 out of 100 for the mobile version and 30 out of 100 for the desktop version. 

**Images**

* Compressed all images 
* Resized the `pizzeria.jpg`

**Javascript**

* One javascript file (analytics.js) was render blocking. I added `async` attribute so that it was removed from critical rendering path
* Moved an anonymous function to the end of HTML

**CSS**

* Added media query to `print.css` 
* Inlined and minified `style.css` and `@font-face` rule 


Now the website scored 95 on mobile and 96 on desktop. 


## Optimize Frames per Second in pizza.html
I did the followings to ensure a frame rate at 60 when scrolling the page.

* Replaced `querySelector` with `getElementById` and `querySelectorAll` with `getElementsByClassName` 
* Reduced pizzas from 200 to 30 in `document.addEventListener`
* Moved variables outside the `for` loop in the `updatePositions` function to make the loop more efficient
* Seperated original `for` loop into two `for` loops to enhance performance
* Added `backface-visibility: hidden;` to `views/css/style.css`


## Reduce time to resize pizza images
I Moved variables from the `for` loop to reduce the time of resizing from 100+ ms to around 1.5 ms. 
