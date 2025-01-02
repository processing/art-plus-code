---
# This is the frontmatter
title: "Movement, Collaboration & Harmony: Technical Steps" # Title and Heading 1
permalink: /movementCollaborationHarmony-steps/ # Give your page a permalink
published: true

---

# Lesson Plans & Technical Steps

## Step 1: Introduction to Variables & Animation
![Animating with P5JS]({{ "/assets/images/curriculum/Unit-5_Sample-2.gif" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/SwhyQV9_v)

You may be familiar with variables that are included with the P5JS library like mouseX and hour(). Here, we’ll make our own variables and manipulate them for our own purposes. 

Variables are essentially containers that store information. In Javascript, variables can contain different types of information from numbers to text (strings) and more. Creating a variable is called ‘declaring’ a variable and saving a value in that variable is called ‘instantiating’ the variable. Let’s take a look at what that looks like: 
```js
let x; // declaring a variable
x = 50; // instantiating the variable
console.log(x); // outputting the value of the variable to the console

let y = 200; // you can declare and instantiate a variable in one line

x = 300; // modifying the value of the variable
console.log(x);

function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(245, 245, 255);

  stroke(0,0,255);
  fill(255)
  circle(x, y, 80); // using the variables, to the computer, this is the same as writing ellipse(300, 200, 80, 80);
}
```

In the code above, we’ve declared and instantiated two variables x and y. First, we saved the value 50 into x. Then, saved the value 300 into x. When you save a new value into a variable with the equal sign, you are essentially replacing the value that was there before with the new value. This is why the circle is drawn at the x position 300 and not 50. 

Variables are useful because it allows us to use the same values in different parts of the code. For instance, with the following code, I have multiple circles drawn in relation to the x and y variables. If I wanted to shift all of the circles to the right, I only need to change one line:
```js
let x = 100;
let y = 100;

function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(245, 245, 255);

  stroke(0,0,255);
  fill(255)
  circle(x, y, 20);
  circle(x, y + 40, 20); // arithmetic operators allow us to draw things in relation to each other
  circle(x + 20, y, 20);
  circle(x + 20, y + 40, 20);
}
```

We can also use arithmetic operators (+ - * /) to manipulate our variables:
```js
let d = 10; // declaring and instantiating a variable
d = d + 10;
console.log(w);

function setup() {
  createCanvas(600, 400);
  frameRate(24) // slowing down the frame rate so we can see the animation a little better
}

function draw() {
  console.log("current frame: " + frameCount); // frameCount is a P5JS variable that shows the number of frames that have elapsed since the canvas loaded
  
  background(245, 245, 255);
  
  fill(0,0,255);
  stroke(0,0,255);
  fill(255)
  circle(200, 200, d); // using the w variable for the width of our circle
  
  d = d + 1; // adding one to the d value every time the draw function loops
  console.log("diameter is: " + d)
}
```

The syntax d = d + 10 like seen here may look really wonky, especially from an algebraic point of view. What this line is saying is instead of replacing the previous value of the variable d with 10, add 10 to the current value. 

You can see that we are using the same logic inside of the draw function, which makes the circle grow. Remember that the code between the draw() function’s curly brackets loops. This means that every time the draw() function loops (24 times a second), 1 will be added to the value of d. This mechanism allows us to create animation effects. The circle here is not actually getting bigger, but is being redrawn with a greater diameter over and over again. 



## Step 2: Controlling Animations with If/Else Statements
![Animating with P5JS]({{ "/assets/images/curriculum/Unit-5_Sample-3.gif" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/F8Bo0cx46)

You can see that in the animation above, the circle does not stop growing. To gain more control of the animation, we can use if/else statements. This example will reset the value of the variables, thereby resetting the animation.
```js
function setup() {
  createCanvas(600, 400);
  frameRate(24)
}

let d = 24; // declaring and instantiating a variable

function draw() {
  background(245, 245, 255);
  
  // drawing the left circle
  fill(0,0,255);
  stroke(0,0,255);
  fill(255);
  circle(200, 200, d); // using the diameter instead of dimensions
  
  console.log("diameter is: " + d);
  d = d + 1; // adding one to the diameter value every time the draw function loops
  
  if (d > 200) {
    d = 10;
  }
}
```

Instead of resetting an animation, you may want the animation to oscillate back and forth. To do this, you can use a combination of variables and arithmetic expressions. We’ll add a variable for a rate of change, in this case, the growth of the circle. 
```js
function setup() {
  createCanvas(600, 400);
  frameRate(24)
}

let l_diameter = 24; // variable for the left circle's diameter
let r_diameter = 50; // variables for the right circle's diameter
let speed = 1; // variable for the change

function draw() {
  background(245, 245, 255);
  
  // drawing the left circle
  fill(0,0,255);
  stroke(0,0,255);
  fill(255)
  circle(200, 200, l_diameter);
  
  l_diameter = l_diameter + 1;
  
  if (l_diameter === 200) { // resetting the l_diameter value
    l_diameter = 10;
  }
  
  // drawing the right circle
  fill(0,0, 255);
  circle(400, 200, r_diameter);
  
  // animating the right circle
  r_diameter = r_diameter + speed; // adding the variable speed instead of 1
  
  // using an if statement to reverse the animation
  if (r_diameter >= 100) {
    speed = speed * -1; // multiplying speed by -1 to set a negative value
  } else if (r_diameter <= 50) {
    speed = speed * -1; // doing the same on the other end
  }
  console.log("r_diameter is: " + r_diameter)
}
```

You can create variables and manipulate them this way for all aspects of your drawing including the color and coordinates! 


## Step 3: Functions
![Creating custom functions.]({{ "/assets/images/curriculum/Unit-5_Sample-4.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/Tw4-5FrJY) 

You may be familiar with P5JS included functions like mouseDragged(). Just like with variables, we can create our own functions to reuse code. This helps keep code modular and efficient. The syntax for creating a function is: 
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

You might notice that this syntax looks very similar to the commands for shapes like ellipse() and rect(). This is because those commands are functions that are included in the P5JS library! Let’s now call the function in the example:
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



## Step 5: Parameters
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

## Step 5: Using Global and Local Variables
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

Functions are important for coding because they allow us to organize our projects in a modular way, that is with multiple pieces making up a whole. See how functions can help us collaborate with code!