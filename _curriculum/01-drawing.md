---
# This is the frontmatter
title: "Digital Drawing Tool: Introduction" # Title and Heading 1
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

### Step A1: Drawing with P5js
[Sample Sketch](https://editor.p5js.org/jyk/sketches/tS5O2kwg9)

Let’s get some code on the board to start fiddling around. When we open the [P5JS web editor](http://editor.p5js.org), we see the following code: 
```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

Our P5JS sketch is divided into 2 sections, function setup() {} and function draw() {}. All of the code between the curly brackets {} after setup() will run once from top to bottom when the page loads. All of the code between the draw() {} curly brackets will repeat.

Let’s modify this code to start drawing. First, we’ll set the size of the canvas to take up the entire width and height of the browser window using the windowWidth and windowHeight variables. windowWidth and windowHeight are examples of variables that come with the P5JS library. We’ll be using a few of these to make our drawing tool. Here, windowWidth is keeping track of the width of the browser, and by using the keyword windowWidth, we are referring to that number. So if the width of your browser window  is 804 and the height of your browser is 476, writing in createCanvas(windowWidth, windowHeight) is the same as writing createCanvas(804, 476). 

Next, we’ll change the color of the background and shape to white using R, G, B values. For commands related to color, we’ll typically use three numbers representing red, green, and blue values. Red, green, and blue are the primary colors for mixing light (positive color system). The maximum value we can put in is 255 and the minimum value is 0.

```js
background(255, 0, 0); 	// 255 red, 0 green, 0 blue makes red
fill(0, 166, 147); 		// 0 red, 166 green, 147 blue makes teal
stroke(228, 204, 255);		// 228 red, 204 green, 255 blue makes lavender
```

We’ll also use the line noStroke() to get rid of the shape’s outline. 

Then we’ll add an ellipse. To draw an ellipse, you set the X position, the Y position, then the width and the height:

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

Next, we’ll use the mouseX and mouseY variables. These are like windowWidth and windowHeight except they are used to keep track of the mouse’s X and Y position. 

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
### Step A2: Making a Drawing Tool
[Sample Sketch](https://editor.p5js.org/jyk/sketches/vyLR0YpM-)

Now that we have the basic interaction mechanism for our drawing tool, we now need to make the drawing ‘stick’ to the canvas. 

Notice that the command to draw the background is in between the draw() curly braces. This means that everytime the code inside the draw function repeats, the background is drawn again over the previous drawing. Sometimes this is a useful mechanism, but not very helpful for our current goal. 

We’ll instead move the background command between the setup() curly brackets. This will make the background draw once when the page loads.

We’ll also add opacity to our color commands. In fill, if we add a fourth value, we can control the opacity of the color. 255 is fully opaque and 0 is completely transparent. 

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
