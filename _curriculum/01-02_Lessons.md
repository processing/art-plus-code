---
# This is the frontmatter
title: "Lost and Found" # Title and Heading 1
permalink: /lostAndFound-lessons/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/curriculum/Unit-1_Sample-2.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-2.gif
    alt: "black circle following a mouse"
    title: "Digital Drawing Tool Step 1"
  - url: /assets/images/curriculum/Unit-1_Sample-3.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-3.gif
    alt: "cursor drawing a black line made up of a series of translucent circles"
    title: "Digital Drawing Tool Step 2"
  - url: /assets/images/curriculum/Unit-1_Sample-4.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-4.gif
    alt: "cursor drawing multiple black arches made up of translucent circles"
    title: "Digital Drawing Tool Step 3"
  - url: /assets/images/curriculum/Unit-1_Sample-5.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-5.gif
    alt: "cursor creating a drawing of vertical blue lines and stamping red ellipses"
    title: "Digital Drawing Tool Step 4"
---
# Lesson Plans & Technical Steps

## 1. Drawing with p5.js
![Following your mouse's x and y position!]({{ "/assets/images/curriculum/Unit-1_Sample-2.gif" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/tS5O2kwg9)

Let’s get some code on the board to start fiddling around. When we open the [p5.js editor](http://editor.p5js.org), we see the following code: 
```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

Our p5.js sketch is divided into 2 sections, function [setup() {}](https://p5js.org/reference/p5/setup/) and function [draw() {}](https://p5js.org/reference/p5/draw/). All of the code between the curly brackets **{}** after setup() will run once from top to bottom when the page loads. All of the code between the draw() {} curly brackets will repeat.

Let’s modify this code to start drawing. First, we’ll set the size of the canvas to take up the entire width and height of the browser window using the [windowWidth](https://p5js.org/reference/p5/windowWidth/) and [windowHeight](https://p5js.org/reference/p5/windowHeight/) variables. windowWidth and windowHeight are examples of variables that come with the p5.js library. We’ll be using a few of these to make our drawing tool. Here, windowWidth is keeping track of the width of the browser, and by using the keyword windowWidth, we are referring to that number. So if the width of your browser window  is 804 and the height of your browser is 476, writing in createCanvas(windowWidth, windowHeight) is the same as writing[ createCanvas(804, 476)](https://p5js.org/reference/p5/createCanvas/). 

Next, we’ll change the color of the [background](https://p5js.org/reference/p5/background/) to white using R, G, B values. For commands related to color, we’ll typically use three numbers representing red, green, and blue values. Red, green, and blue are the primary colors for mixing light (positive color system). The maximum value we can put in is 255 and the minimum value is 0.

```js
background(255, 0, 0); 	// 255 red, 0 green, 0 blue makes red
fill(0, 166, 147); 		// 0 red, 166 green, 147 blue makes teal
stroke(228, 204, 255);		// 228 red, 204 green, 255 blue makes lavender
```

We’ll also use the line [noStroke()](https://p5js.org/reference/p5/noStroke/) to get rid of the shape’s outline. 

Then we’ll add an [ellipse](https://p5js.org/reference/p5/ellipse/). To draw an ellipse, you set the X position, the Y position, then the width and the height:

```js
function setup() { // this function runs once when the page loads
  createCanvas(windowWidth, windowHeight); // making the dimensions of the canvas take up the entire window
  background(255,255,255); // making the background color white
} // end of the setup() function

function draw() { // this function will loop 60x a second
  background(255,255,255);
  noStroke();
  fill(0,0,0); // fill(r, g, b)
  ellipse(100, 100, 40, 40); // ellipse(x, y, w, h);
}
```

Now you should see a little circle on your white page! Try changing around the numbers so that you can get a sense of what the different components are doing. 

Next, we’ll use the [mouseX](https://p5js.org/reference/p5/mouseX/) and [mouseY](https://p5js.org/reference/p5/mouseY/) variables. These are like windowWidth and windowHeight except they are used to keep track of the mouse’s X and Y position. 

You can output messages to the console to keep track of changing values like this one:
```js
console.log("your message between these quotation marks");
console.log(nameOfAVariable);
console.log("your message between these quotation marks" + nameOfAVariableNoQuotes);
```

Notice how the messages are popping up over and over again in the console with different numbers. This is because the code in the draw function is looping. That means that the command to print a message in the console is being executed again and again and the mouseX and mouseY values are constantly being updated. 

You can also try substituting any of the numbers in the sketch with mouseX and mouseY to see how they might respond to the movement of the mouse.

```js
function draw() { // this function will loop 60x a second
  background(255,255,255);
  noStroke();
  fill(0,0,0);
  console.log("mouse X: " + mouseX); // displaying the mouseX value in the console
  console.log("mouse Y: " + mouseY);
  ellipse(mouseX, mouseY, 40, 40); // making the circle move with the mouse
}
```
## 2. Making a Drawing Tool
!['Drawing' with the mouse]({{ "/assets/images/curriculum/Unit-1_Sample-3.gif" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/vyLR0YpM-)

Now that we have the basic interaction mechanism for our drawing tool, we now need to make the drawing ‘stick’ to the canvas. 

Notice that the command to draw the background is in between the **draw()** curly braces. This means that everytime the code inside the draw function repeats, the background is drawn again over the previous drawing. Sometimes this is a useful mechanism, but not very helpful for our current goal. 

We’ll instead move the background command between the **setup()** curly brackets. This will make the background draw once when the page loads.

We’ll also add opacity to our color commands. In [fill](https://p5js.org/reference/p5/fill/), if we add a fourth value, we can control the opacity of the color. 255 is fully opaque and 0 is completely transparent. 

Now, we have something more like a basic drawing tool. Try modifying the size, color, and opacity of the circle to customize the form of the line. 

```js
function setup() { // this function runs once when the page loads
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); // making the background color white
}

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0,20);
  ellipse(mouseX, mouseY, 40, 40);
} // end of the draw() function
```

## 3. Refining the Tool for Drawing
![Making the drawing tool more user friendly!]({{ "/assets/images/curriculum/Unit-1_Sample-4.gif" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/sSzIOAtiP)


Let’s find some way to make this drawing tool more conducive to the experience of drawing by adding some controls. 

The first thing that we’ll use is the [mouseDragged()](https://p5js.org/reference/p5/mouseDragged/) function. You’ll notice that the syntax for this is very similar to the setup() {} and draw() {} sections. These are called **functions**. Functions are a way to group a section of code together. This lets us control when a selection of code lines will execute. The way we make a function is: 

```js
function functionName() { // beginning of function
// everything in between these curly brackets 
// will run when the function is called
} // end of function
```

Like variables, the p5.js library comes with functions that will be triggered, or called automatically for specific purposes. For instance, the setup() function automatically runs once when the browser window opens. We’ll try out the mouseDragged() function which will run while the mouse is clicked and dragged:

```js
function mouseDragged() {
// these lines will run when
// the mouse is clicked and dragged
}
```

Let’s move the drawing commands from between the draw() curly braces to the mouseDragged() curly braces. Now, our tool will only draw when the mouse is dragged! 

```js
function setup() {  
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); 
} // end of the setup() function

function draw() { 

} // end of the draw function

function mouseDragged() {
  noStroke(); 
  fill(0,0,0, 20);
  ellipse(mouseX, mouseY, 40, 40);
}
```

In addition to mouseDragged(), there are several functions that we can use to make use of the [mouse input](https://p5js.org/reference/#Events). Try adding one or many of these to the bottom of your code:
- function [mouseClicked()](https://p5js.org/reference/p5/mouseClicked/) { ... }
- function [mousePressed()](https://p5js.org/reference/p5/mousePressed/) { ... }
- function [mouseMoved()](https://p5js.org/reference/p5/mouseMoved/) { ... }
- function [mouseReleased()](https://p5js.org/reference/p5/mouseReleased/) { ... }
- function [mouseWheel()](https://p5js.org/reference/p5/mouseWheel/) { ... }
- function [doubleClicked()](https://p5js.org/reference/p5/doubleClicked/) { ... }


We can also use the [save()](https://p5js.org/reference/p5/save/) command to save the drawing. We’ll combine that with the [doubleClicked()](https://p5js.org/reference/p5/doubleClicked/) function so that when the mouse is double-clicked, a copy of our drawing will be saved to the computer. 

```js
function setup() {  
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); 
  frameRate(60); // this line will adjust how fast the draw() background repeats
} // end of the setup() function

function draw() { 

}

function mouseDragged() {
  noStroke(); 
  fill(0,0,0, 20);
  ellipse(mouseX, mouseY, 40, 40);
}

function doubleClicked() {
  save('my_drawing.png');
}
```

If you want to control the sensitivity of the drawing tool, you can also adjust the rate at which the draw() function repeats using the [frameRate()](https://p5js.org/reference/p5/frameRate/) command: 

```js
function setup() {  
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); 
  frameRate(60); // this line will adjust how fast the draw() background repeats
} // end of the setup() function

function draw() { 

}

function mouseDragged() {
  noStroke(); 
  fill(0,0,0, 20);
  ellipse(mouseX, mouseY, 40, 40);
}

function doubleClicked() {
  save('my_drawing.png');
}
```

## 4. Extending the Tool with Complexity
![Adding more features to the drawing tool.]({{ "/assets/images/curriculum/Unit-1_Sample-5.gif" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/AbvL7apEE)


Now that we have the basics for a drawing tool, we can refine the details of the tool to design a line to best capture movement and support our drawing’s goals. 

You use a variety of shapes in addition to the ellipse to create unique lines:
- [ellipse(x, y, w, h);](https://p5js.org/reference/p5/ellipse/)
- [rect(x, y, w, h);](https://p5js.org/reference/p5/rect/)
- [line(x1, y1, x2, y2);](https://p5js.org/reference/p5/line/) *(Note that for the line, you'll need a stroke() command)*
- [triangle(x1, y1, x2, y2, x3, y3);](https://p5js.org/reference/p5/triangle/)
- [quad(x1, y1, x2, y2, x3, y3, x4, y4);](https://p5js.org/reference/p5/quad/)

You can also incorporate key functions. These are similar to the mouse functions, but instead are triggered by [key inputs](https://p5js.org/reference/#Events). You can add these functions to the bottom of your code:
- function [keyPressed()](https://p5js.org/reference/p5/keyPressed/) { ... }
- function [keyReleased()](https://p5js.org/reference/p5/keyReleased/) { ... }

You can mix and match these components with the ones already being used to add complexity to the drawing tool. 

```js
function setup() {  
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); 
  frameRate(20); // this line will adjust how fast the draw() background repeats
} // end of the setup() function

function draw() { 

}

function mouseDragged() {
  stroke(0, 0, 100, 60);
  strokeWeight(2);
  line(mouseX, mouseY -10, mouseX, mouseY + 10)
}

function keyPressed() {
  noStroke(); 
  fill(mouseX,0,0, mouseY);
  ellipse(mouseX, mouseY, 60, 20);
}

function doubleClicked() {
  save('my_drawing.png');
}
```
