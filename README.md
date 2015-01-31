# P4
Website Performance Optimization

This project is also hosted here:
The index page:
http://knitaswatch.com/p4/

The pizza page:
http://knitaswatch.com/p4/views/pizza.html


# Steps to run the application:

-Open pizza.html in a Google Chrome browser

-Open Developer Tools (Ctrl + Shift + I), and go to Timeline

-Press the record button, and scroll from top to bottom and back to the top
 multiple times before pressing the record button again to stop recording. 
 
-Wait for the recorded events timeline, and check to see if all colored bars are 
under the 6OFPS line.

-The application works as required if the frame rate is 60FPS or better

---
-Open index.html in the browser to view the page, and click on the links present to
view other project pages

-To check the PageSpeed score, go to -
 https://developers.google.com/speed/pagespeed/insights/
 and enter the page URL (the page is hosted at http://knitaswatch.com/p4/)
 
-The application works as required if the score for both 
 mobile and desktop versions is over 90 percent

# Changes made to optimize the pizza page (main.js):

In main.js:

-In the updatePositions function, stored the value of document.body.scrollTop/1250
outside the for loop so it doesn't have to be recalculated with every iteration

-Reduced the number of pizzas from 200 to 120 in the final function that generates 
sliding pizzas.

-Wrapped the for loop that creates and appends all of the pizzas to 
the page in a window.onload event

-reduced paint time by applying translate3d (webkit transform) to the mover class in 
the updatePositions function

-commented out / removed some of the fixed css properties for the mover class from
the final JS function and added those directly to the stylesheet in pizza.js

---
To optimize pizza resizing in main.js:

-Stored document.querySelector("#pizzaSize") in a variable outside the switch 
statement so it doesn't have to be recalculated in all three cases

-combined the two switch statements into one

# General:
-Compressed all images using compressor.io

-Optimized CSS delivery by either using internal stylesheets or loading css 
resources after initial loading of content using a JS function

-Optimized Google webfont delivery as above

-Used the media attribute (print and portrait) in the css links where applicable

-Loaded JS files asynchronously where possible by using the async attribute

---
"I hereby confirm that this submission is my work and that I am abiding by guidelines within the Student Code of Conduct in the Nanodegree student handbook."
