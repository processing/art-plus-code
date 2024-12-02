---
# This is the frontmatter
title: "Digital Drawing Tool: Capturing Movement with Digital Lines" # Title and Heading 1
permalink: /1-drawing/ # Give your page a permalink

gallery: # Below is for including an image gallery
  - url: /assets/images/unit_a_example-1.png
    image_path: /assets/images/unit_a_example-1.png
    alt: "black and white abstract drawing of curves"
    title: "Sample Drawing 1"
  - url: /assets/images/unit_a_example-2.png
    image_path: /assets/images/unit_a_example-2.png
    alt: "simplified line drawing of a face with red oval pattern"
    title: "Sample Drawing 2"

---

### Step 1: Drawing with P5js
Let’s start fiddling around with some code. When we open the [P5JS web editor](http://editor.p5js.org), we see the following: 
```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

Our P5JS sketch is divided into 2 sections, function setup() {} and function draw() {}. All of the code between the curly brackets {} after setup() will run once from top to bottom when the page loads. All of the code between the draw() {} curly brackets will repeat.

Let’s modify this code to start drawing. First, we’ll change the color of the background and shape to white using R, G, B values. For commands related to color, we’ll typically use three numbers representing red, green, and blue values. Red, green, and blue are the primary colors for mixing light (positive color system). The maximum value we can use is 255 and the minimum value is 0.

```js
background(255, 0, 0); 	// 255 red, 0 green, 0 blue makes red
fill(0, 166, 147); 		// 0 red, 166 green, 147 blue makes teal
stroke(228, 204, 255);		// 228 red, 204 green, 255 blue makes lavender
```

We can also use the command noStroke() to get rid of the shape’s outline. 

Then we’ll add an ellipse. To draw an ellipse, you set the X position, the Y position, then the width and the height:

```js
function setup() { // this function runs once when the page loads
  createCanvas(400, 400); // making a canvas that is 400px by 400px
} // end of the setup() function

function draw() { // this function will loop 60x a second
  background(255,255,255);
  noStroke();
  fill(0,0,0); // fill(r, g, b)
  ellipse(100, 100, 40, 40); // ellipse(x, y, w, h);
}
```

Now you should see a little black circle on your white page! Try changing around the numbers so that you can get a sense of what the different components are doing. 

Next, we’ll use the mouseX and mouseY variables. These are dynamic variables that come with the P5JS library. You can output messages to the console to keep track of changing values like this one:
```js
console.log("the value of mouseX is: " + mouseX);
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
### Step 2: Making a Drawing Tool
Now that we have the basic interaction mechanism for our drawing tool, we now need to make the drawing ‘stick’ to the canvas. 

Notice that the command to draw the background is in between the draw() curly braces. This means that everytime the code inside the draw function repeats, the background is drawn again over the previous drawing. Sometimes this is a useful mechanism, but not very helpful for our current goal. 

We’ll instead move the background command to between the setup() curly brackets. This will make the background draw once when the page loads, but not again afterwards.

Now, we have something more like a basic drawing tool. Try modifying the color and dimensions of the circle to customize the form of the line being drawn. 

```js
function setup() { // this function runs once when the page loads
  createCanvas(400, 400);
  background(255,255,255); // making the background color white
}

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0);
  ellipse(mouseX, mouseY, 40, 40);
} // end of the draw() function
```

### Step 3: Refining the Quality of the Lines
Now that we have a basic drawing tool, we can add some additional code to make the line being drawn more sophisticated! 

**Shapes**
You use a variety of shapes to create unique lines. In addition to the ellipse, these include rect(), line(), triangle() and quad():
```js
ellipse(x, y, w, h);
rect(x, y, w, h);
line(x1, y1, x2, y2); // note that for the line, you'll need a stroke() command.
triangle(x1, y1, x2, y2, x3, y3);
quad(x1, y1, x2, y2, x3, y3, x4, y4);
```
```js
function setup() { // this function runs once when the page loads
  createCanvas(400, 400);
  background(255,255,255); // making the background color white
}

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0);
  rect(mouseX, mouseY, 10, 60); // using a long, skinny rectangle to get something similar to a callligraphy pen
} // end of the draw() function
```

**Full Screen Canvas**
We can set the size of the canvas to take up the entire width and height of the browser window using the windowWidth and windowHeight variables. Like mouseX and mouseY, windowWidth and windowHeight are dynamic variables that come with the P5JS library. Here, windowWidth is keeping track of the width of the browser, and by using the keyword windowWidth, we are referring to that number. So if the width of your browser window  is 804 and the height of your browser is 476, writing in createCanvas(windowWidth, windowHeight) is the same as writing createCanvas(804, 476): 
```js
function setup() { // this function runs once when the page loads
  createCanvas(400, 400);
  background(255,255,255); // making the background color white
}

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0);
  rect(mouseX, mouseY, 10, 60);
} // end of the draw() function
```

**Opacity**
If you add a fourth number (or parameter) to a color command, you can control the opacity of the color. 255 is fully opaque and 0 is completely transparent. By adding a parameter for opacity to the fill command, we can give the line being drawn more depth by making it semi-transparent.
```js
function setup() { // this function runs once when the page loads
  createCanvas(400, 400);
  background(255,255,255); // making the background color white
}

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0, 30);
  rect(mouseX, mouseY, 10, 60);
} // end of the draw() function
```

**Sensitivity**
If you want to control the sensitivity of the drawing tool, you can also adjust the rate at which the draw() function repeats using the frameRate() command. This command allows you to control how frequently the code between the draw function repeats (frames per second) by slowing it down, you can make the refresh rate slower, thereby making the drawing tool less sensitive: 
```js
function setup() {  
  createCanvas(windowWidth, windowHeight);
  background(255,255,255); 
  frameRate(20); // this line will adjust how fast the draw() background repeats
} // end of the setup() function

function draw() { // this function will loop 60x a second
  noStroke();
  fill(0,0,0, 30);
  rect(mouseX, mouseY, 10, 60);
} // end of the draw() function
```

*Using just a few lines of code, we've now created a tool for drawing! Check out the next steps to add complexity using mouse and key inputs!*


## Assessment Activities
*Questions to consider for discussion and reflection:*
- Describe some of the P5JS elements that you used for your drawing tool (shapes, inputs, etc)
- Why did you make the decision to design your tool in the way that you did? E.g. did you create a translucent effect to mimic charcoal? Did you make the lines wider to have a more playful effect?
- What were some of the challenges that you ran into?
- How does your drawing process compare when drawing in a physical or digital setting?
- If you had more time (and technical knowledge) how would you modify your design tool?


## Checking for Understanding
*Do students grasp the core concepts of the topic?*
- Do their drawings and digital tools demonstrate deliberate choices behind the lines used in their drawings?
- Do the lines in the digital and physical drawings align with the goals of their drawing (e.g fits in with a descriptor or concept).
- Is the code written by the student free of errors that prevent the code from working?

*Are the students comfortable with the technical aspects of the topic?*
- Do they make use of multiple tools discussed in the lesson? How much did they adapt the example code to fit their drawing’s goals?
- Are the methods being used deliberately and in order to support the purpose of the sketch? Or are they copying and pasting without much thought?
- Are the student’s questions specific to issues in their project? Or is it just ‘it’s not working’?

*Are the students using their creative and visual communication skills?*
- How many different techniques or combination of tools did they use before settling on an idea? Or did they stop at the first idea they came up with?
- Did the student extend themself by looking at tools beyond the demonstration?
- Is the student demonstrating a similar amount of care and attention to detail in their digital as well as physical drawings? 

*How are the students keeping track of their personal and artistic growth?*
- Was the student’s summary of their tool and drawings provide a clear and specific overview of their process?
- How did the student articulate the difference between the digital and physical drawing processes?
- How did the student manage frustration or challenges throughout the process and how did they comment on these challenges after they were resolved?
  
