---
# This is the frontmatter
title: "Drawing Machine" # Title and Heading 1
permalink: /drawingMachine-lessons/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/thumbnails/unit4.png
    image_path: /assets/images/thumbnails/unit4.png
    alt: "Screenshot of a digital mask using the p5.js web editor"
    title: "Sound Reactive Mask"

---
# Lesson Plans & Technical Steps

## 1: Functions
![Creating custom functions.]({{ "/assets/images/curriculum/Unit-5_Sample-4.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/Tw4-5FrJY) 

You may be familiar with p5.js included functions like mouseDragged(). Just like with variables, we can create our own functions to reuse code. This helps keep code modular and efficient. The syntax for creating a function is: 
```js
function functionName() { // beginning of function
// everything in between these curly brackets 
// will run when the function is called
} // end of function
```

Typically, we write functions near the bottom of the code, after the draw() function’s curly braces. This example uses a function to draw an eye:
```js 
function setup() {
  createCanvas(600, 600);
}

function draw() {
  background(255, 225, 255);
  noStroke();
  fill(255, 255, 100);
  ellipse(300, 300, 400, 400);
}

function eye() {
  strokeWeight(1);
  fill(255);
  ellipse(400, 280, 60, 60);
  fill(0, 0, 0);
  ellipse(400, 285, 40, 40);
}
```

You’ll notice that nothing happened. This is because in order for the code inside of a function’s curly braces to execute, the function needs to be called. To do so, you write the name of the function followed by parentheses: 

```js
functionName();
```

You might notice that this syntax looks very similar to the commands for shapes like ellipse() and rect(). This is because those commands are functions that are included in the p5.js library! Let’s now call the function in the example:
```js
function setup() {
  createCanvas(600, 600);
}

function draw() {
  background(255, 225, 255);
  noStroke();
  fill(255, 255, 100);
  ellipse(300, 300, 400, 400);
  eye(); // calling the eye function
}

function eye() { // setting up the eye function
  strokeWeight(1);
  fill(255);
  ellipse(400, 280, 60, 60);
  fill(0, 0, 0);
  ellipse(400, 285, 40, 40);
} // end of the eye function
```

## 2: Parameters
![Modifying functions with parameters.]({{ "/assets/images/curriculum/Unit-5_Sample-5.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/SoSuHE6Cl) 

We can call a function as many times as we want, by writing the command to call the function again and again:
```js
eye();
eye();
```

But this is not very helpful as it will draw the same drawing in the same place. To make the function more flexible, we will use parameters. A parameter is a useful way of passing value into a function:
```js
function myFunction(parameter1, parameter2) {
	console.log("parameter 1 is: " + parameter1);
	console.log("parameter 2 is: " + parameter2);
}

myFunction(10, 100); // here, we are passing the value 10 into parameter1, and 100 into parameter2
myFunction(77, 81); // here, we are passing the value 77 into parameter1, and 81 into parameter2
```

Again, you’ll see that the syntax looks a lot like the commands for drawing shapes. That is because the values set for things like x, y, width and height are parameters for the shape drawing functions. One easy way to think about functions is that we are creating our own drawing commands.
```js
function setup() {
  createCanvas(600, 600);
}

function draw() {
  background(255, 225, 255);
  noStroke();
  fill(255, 255, 100);
  ellipse(300, 300, 400, 400);
  eye(200, 280); // left eye
  eye(400, 280); // right eye
}

function eye(x, y) {
  strokeWeight(1);
  fill(255);
  ellipse(x, y, 60, 60); // using x and y instead of hardcoded numbers
  fill(0, 0, 0);
  ellipse(x, y+5, 40, 40);
}
```

Parameters are essentially variables that are a part of a function. In this example, we replaced the set numbers for the x and y coordinates of an eye with the x and y parameters. That way, those values are actually decided when the function eye() is called in the draw function, allowing us to reuse the same components but with more control.

The scope of parameters are limited to the curly braces of a function. In other words, the variables x and y that are being used in the function eye won’t be recognized outside of the eye() function’s curly braces. If you try to use x and y outside of the eye() function’s curly braces, you’ll get an error. This also means that you can use the labels x and y for other functions. 

You can set as many parameters as you’d like to make your function work for you.
```js
function setup() {
  createCanvas(600, 600);
}

function draw() {
  background(255, 225, 255);
  noStroke();
  fill(255, 255, 100);
  ellipse(300, 300, 400, 400);
  eye(200, 280, 48, 30, 11, 100); // left eye
  eye(400, 280, 0, 56, 200, 80); // right eye
  eye(300, 200, 0, 217, 108, 40); // third eye
  
}

function eye(x, y, r, g, b, size) {
  strokeWeight(1);
  fill(255);
  ellipse(x, y, size, size);
  fill(r,g,b);
  ellipse(x, y+5, size * .67, size * .67);
  fill(0);
  ellipse(x, y+5, size/2, size/2);
}
```

## 3: Using Global and Local Variables
![Global and Local Variables]({{ "/assets/images/curriculum/Unit-5_Sample-6.gif" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/tuuCIAUrm) 

When a variable’s scope is limited to the curly braces of a single function, that is called a local variable. Variables that are declared outside of any function, and can be used inside any function are called global variables. Programmers use a combination of local and global variables to serve different purposes. In our case, we’ll use local variables to set the rules of our drawing components and global variables to animate them.

In this example, we will use global variables leftEye, rightEye, and sideEye with if/else statements to make the pupil/irises of the eye go from side to side:
```js
function setup() {
  createCanvas(600, 600);
}

let leftEye = 200;
let rightEye = 400;
let sideEye = 0.25;

function draw() {
  background(255, 225, 255);
  noStroke();
  fill(255, 255, 100);
  ellipse(300, 300, 400, 400);
  eye(200, 290, leftEye); // left eye
  eye(400, 290, rightEye); // right eye
  
  if (leftEye >= 215 || leftEye < 185) {
    sideEye *= -1;
  }
  
  leftEye += sideEye;
  rightEye += sideEye; // we don't need another if statement because we want the eyes to move in the same way
}

function eye(x, y, pupil) {
  strokeWeight(1);
  fill(255);
  ellipse(x, y, 100, 80);
  fill(82, 57, 0);
  ellipse(pupil, y, 60, 60);
  fill(0);
  ellipse(pupil, y, 40, 40);
}
```

**🎨  In our Drawing Tool:** We’ve made color changes for one key, but now we can assign different colors to different keys! Read the comments below to see how we’ve added to our initial If-Then-Else statement by adding Else-if. 

```jsx
function keyPressed() { // When the key is pressed

  if (key == "r") {  // And if the key is "r" , fill the circle with red 
    fill(255,0,0);
  } else if (key == "g") {  // Otherwise, if the key is "g" , fill the circle with green 
    fill(0,255,0); 
  } else if (key == "b"){   // Otherwise, if the key is "b" , fill the circle with blue 
    fill(0,0,255);
  } else {      // And, if the key pressed is anything else other than r, g, b, or x, fill the circle with white 
	  fill(255);
	  }
}
```

Functions are important for coding because they allow us to organize our projects in a modular way, that is with multiple pieces making up a whole. See how functions can help us collaborate with code!


<!-- ### Grade 9~12

#### Make a Rainbow Brush!

Because the hue property of the [HSB color model](/lostAndFound-lessons/2#e-color-modes) uses the 0~360 range to cycle through the color wheel, we can make a rainbow brush tha -->