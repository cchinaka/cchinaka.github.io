## Website Performance Optimization portfolio project - final working nicely

My Final Project!

Final Links of interest:<br/>
1. My Page Speed Test: <a href="cchinaka.github.io/webopt/index.html">cchinaka.github.io/webopt/index.html</a>
2. Scrolling optimizations: <a href="https://cchinaka.github.io/webopt/views/pizza.html">https://cchinaka.github.io/webopt/views/pizza.html</a>


##Work Done

### Page Speed optimizations:
1. Added media="print" to print.css as it's only required on a print.
2. Moved a minimized version of style.css content directly into the pages that required it, thereby eliminating the need for it as a critical resource
3. Set a width to all of the images to help the browser render it faster, removed the width image setting of 100%.
4. Not sure where to setup my caching on the server as providing it back in github for viewing, but i would like to apply the following to the fonts
5. Have the server provide a long-lived max-age timestamp as i don't expect to change this font. (COULD NOT DO)
6. I used webfontloader, loaded asynchronously, to load the fonts as it reduces the number of critical resources by one and has the added advantage of rendering the font once available
7. Images got squished to an average percentage of 80% reduction in image size

####Note: 
** The new pagespeed - Mobile - 95/100; Desktop: 96/100

### Scrolling - Jank Fixes:

*All work done was in views/js/main.js*

1. changePizzaSizes:forced synchronous layout detected
Solution applied for forced synchronous layout detected here. The fix applied was to separate the read of element attributes AND the application of new values to them.

2. updatePositions():
Solutions the fix applied here is two fold.
a. The updatePositions has been applied to requestAnimationFrame to ensure the process kicks off as close to the frame start as possible. and reduce jank
b. within doActualUpdatePositions: forced synchronous layout detected in update style left attribute of elements.
    The fix applied was, again, to separate the read of element attributes AND the application of new values to them.
3. Optimized Image pizzeria.jpg. INCLUDED an alternative image of larger size pizzeria-lg.jpg

####Note:
1. I think the animation can be further optimized by moving the animations to CSS.


### Resources Referenced
**<a href="http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/">http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/</a>
**<a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization?hl=en">https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization?hl=en</a>



#I feel so good!!
