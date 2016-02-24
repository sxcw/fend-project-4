# Website Performance Optimization 

## How to Run
1. Clone the repository or download the zip file
2. Open `index.html` in your browser

## Optimize PageSpeed Insights score for index.html

For this project, I optimized Cameron Pittman's portfolio website. First I tested this site on Google PageSpeed Insights (https://developers.google.com/speed/pagespeed/). This website scored 28 out of 100 for the mobile version and 30 out of 100 for the desktop version. 

** Images **

* Compressed all images 
* Resized the `pizzeria.jpg`

** Javascript **

* One javascript file (analytics.js) was render blocking. I added `async` attribute so that it was removed from critical rendering path
* Moved an anonymous function to the end of HTML

** CSS **

* Added media query to `print.css` 
* Inlined and minified `style.css` and `@font-face` rule 


Now the website scored 95 on mobile and 96 on desktop. 


## Optimize Frames per Second in pizza.html

* Replaced `querySelector` with 'getElementById' and `querySelectorAll` with `getElementsByClassName` 
* 
