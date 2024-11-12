---
# This is the frontmatter
title: "Topic A" # Title and Heading 1
permalink: /unit-a/ # Give your page a permalink
hidden: false # Remove this line for any units you want added to the sidebar navigation

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

# Capturing Movement with Digital Lines

> A line could also be defined as a dot in motion, or the history of a dot’s movement, since, when we make a continuous mark or a line, we make it by placing a marker point on a surface and moving it along, leaving the formed marks as a record.” 
>
> \- Donis A. Dondis, A Primer of Visual Literacy

In many of her drawings, artist Christine Sun Kim captures the motions of sign language through lines. Words like “future” and “time” are depicted with arching curves, mimicking the vertical and horizontal movements of the hand making the sign in ASL. The scale of Kim’s work ranges from intimate drawings to monumental murals. In each of her works, her deliberate choices around the form, weight, and composition of the lines she uses are essential in communicating a unique sense of motion and personality. 

In this topic, we’ll use P5JS to design a unique drawing tool. We’ll design the drawing tool to be compatible with an idea for a drawing. Then we’ll use the tool to create and then save a drawing. 

{% include gallery caption="Create your own drawing tool using P5JS!" %}

## Objectives
- Gaining insight into diverse practices in traditional and contemporary drawing
- Understanding the relationship between drawing tools and artistic intention
- **Visual Arts Vocabulary**: line, space, value, form, texture, color


## Technical Terms & P5JS Elements
- functions: [setup()](https://p5js.org/reference/p5/setup/), [draw()](https://p5js.org/reference/p5/draw/)
- canvas methods and variables: [windowWidth](https://p5js.org/reference/p5/windowWidth/), [windowHeight](https://p5js.org/reference/p5/windowHeight/), [background()](https://p5js.org/reference/p5/background/), [frameRate()](https://p5js.org/reference/p5/frameRate/)
- drawing methods: [rect()](https://p5js.org/reference/p5/rect/), [ellipse()](https://p5js.org/reference/p5/ellipse/),  [fill()](https://p5js.org/reference/p5/fill/), [stroke()](https://p5js.org/reference/p5/stroke/), [noStroke()](https://p5js.org/reference/p5/noStroke/)
- mouse variables and methods: [mouseX](https://p5js.org/reference/p5/mouseX/), [mouseY](https://p5js.org/reference/p5/mouseY/), [mouseDragged()](https://p5js.org/reference/p5/mouseDragged/), [doubleClicked()](https://p5js.org/reference/p5/doubleClicked/)
- [save()](https://p5js.org/reference/p5/save/)
- console.log()

  
## References & Artworks for Discussion: Line Quality
* A Primer of Visual Literacy, Donis A. Dondis
* [Art21: Christine Sun Kim](https://art21.org/watch/art-in-the-twenty-first-century/s11/christine-sun-kim-in-friends-strangers/)
* Christine Sun Kim, [Time Owes Me Rest Again](https://queensmuseum.org/exhibition/christine-sun-kim/), 2022, Queens Museum
* Christine Sun Kim, [Too Much Future](https://whitney.org/exhibitions/christine-sun-kim), 2018, Whitney Museum
* Hilma af Klint, [Spiritual Drawing](https://www.guggenheim.org/audio/track/spiritual-drawings-of-the-five-ca-1903-04), ca. 1903, Guggenheim Museum
* Jean-Michel Basquiat, [Untitled](https://www.moma.org/collection/works/34633?artist_id=370&page=1&sov_referrer=artist), 1981, Museum of Modern Art
* Wassily Kandinsky, [Untitled (drawing for Diagram 17)](https://artmuseum.mtholyoke.edu/object/untitled-drawing-diagram-17), 1925, Mount Holyoke College Art Museum
* William Kentridge, [Learning the Flute](https://www.moma.org/collection/works/91559), 2003, Museum of Modern Art
* Elizabeth Peyton, [Craig in Tokyo](https://rubellmuseum.org/elizabeth-peyton), 1997, Rubell Museum


## Timeline
This project will take approximately two to three 45minute sessions:
1. Discussing artists and line, Warm-up Exercises, Introduction to P5JS (Step A1)
2. Creating a drawing tool (A2 - A3), Extending the tool (A4)
3. Finishing the tool (A4), Using the Tool & Sharing Out (Assessment)

### Warm-Up Exercises
Some options for unplugged exercises:
- Blind Contour Drawing
  - Using different drawing utensils (pencil, marker, charcoal, ink) students create blind contour drawings of a single object. Comparing the different drawings, students discuss how the quality of the lines affects the tone and effect of the drawing. 
  - Divide students into pairs and have them create blind contour drawings of each other using different drawing materials. Students discuss how the features of the lines made by different drawing tools supports or doesn’t support the ‘portrait’ of their classmate. 
  - Once the initial P5JS drawing tool is completed, students use the drawing tool they designed to create a blind contour drawing. Compare the drawings with the ones they did using physical materials. Students can then adjust their drawing tool to modify the features. 

- Depicting Movement with Lines
  - Provide students with a simple reference object for drawing (e.g. cube, pencil, eraser) and multiple sheets of paper. For 3 minutes at a time, have random words related to motion (fast, awkwardly, quietly, laboriously) displayed on the board. Have students draw the object moving according to the word on the board.
  - Have students display their work on tables or the board according to the descriptors (e.g. all the quickly drawings on one table). Discuss what are qualities the images have in common for different descriptors. 
  - Students choose one descriptor, and create an intermediate sketch depicting that descriptor. 
  - Students use the P5JS drawing tool to create drawings of the descriptors (or chosen one). Students discuss the difference between digital and physical drawings and compare the drawing experiences.

- Make Your Own Paintbrush
  - Using found materials, students create their own paintbrush. While creating a drawing with their brush, students make observations about the relationship between the shape of their brush and the lines they are creating.
 
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

### Step A3: Refining the Tool for Drawing
[Sample Sketch](https://editor.p5js.org/jyk/sketches/sSzIOAtiP)

Let’s find some way to make this drawing tool more conducive to the experience of drawing by adding some controls. 

The first thing that we’ll use is the mouseDragged() function. You’ll notice that the syntax for this is very similar to the setup() {} and draw() {} sections. These are called functions. Functions are a way to group a section of code together. This lets us control when a selection of code lines will execute. The way we make a function is: 

```js
function functionName() { // beginning of function
// everything in between these curly brackets 
// will run when the function is called
} // end of function
```

Like variables, the P5JS library comes with functions that will be triggered, or called automatically. For instance, the setup() function automatically runs once when the browser window opens. We’ll try out the mouseDragged() function which will run while the mouse is clicked and dragged:

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

In addition to mouseDragged(), there are several functions that we can use to make use of the mouse input:
```js
mouseClicked()
mousePressed()
mouseMoved()
mouseReleased()
mouseWheel()
doubleClicked()
```

We can also use the save() command to save the drawing. We’ll combine that with the doubleClicked() function so that when the mouse is double-clicked, a copy of our drawing will be saved to the computer. 

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

If you want to control the sensitivity of the drawing tool, you can also adjust the rate at which the draw() function repeats using the frameRate() command: 

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

### Step A4: Extending the Tool with Complexity
[Sample Sketch](https://editor.p5js.org/jyk/sketches/AbvL7apEE)

Now that we have the basics for a drawing tool, we can refine the details of the tool to design a line to best capture movement and support our drawing’s goals. 

You use a variety of shapes instead of the ellipse to create unique lines:

```js
ellipse(x, y, w, h);
rect(x, y, w, h);
line(x1, y1, x2, y2); // note that for the line, you'll need a stroke() command.
triangle(x1, y1, x2, y2, x3, y3);
quad(x1, y1, x2, y2, x3, y3, x4, y4);
```

You can also incorporate key functions. These are similar to the mouse functions, but instead are triggered by key inputs.
```js
keyPressed()
keyReleased()
```

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

## Assessment Activities

Once ready, students should use the drawing tool they designed to create a drawing:
- Descriptors, using the same descriptors from the warm-up activities, students can create a drawing that depicts an object moving in a specific manner (slowly, hurriedly, loudly)
- Creating a blind contour drawing of the same subject that they did in the warm-up
- A common still-life arrangement: the class creates drawings of the same still, life arrangement.

Once the drawings are complete, they should be saved to the computer. It is recommended that the drawings are uploaded to a shared folder on Google Drive or a class’s LMS. The drawings can then be printed out to be displayed.

Students can also share their tools and resulting drawings. Questions to consider for discussion and reflection:
- Describe some of the P5JS elements that you used for your drawing tool (shapes, inputs, etc)
- Why did you make the decision to design your tool in the way that you did? E.g. did you create a translucent effect to mimic charcoal? Did you make the lines wider to have a more playful effect?
- What were some of the challenges that you ran into?
- Looking at the digital and physical drawings that you made, what are some observations that you make about the result?
- How does your drawing process compare when drawing in a physical or digital setting?
- If you had more time (and technical knowledge) how would you modify your design tool?


## Checking for Understanding

Do students grasp the core concepts of the topic?
- Do their drawings and digital tools demonstrate deliberate choices behind the lines used in their drawings?
- Do the lines in the digital and physical drawings align with the goals of their drawing (e.g fits in with a descriptor or concept).
- Is the code written by the student free of errors that prevent the code from working?

Are the students comfortable with the technical aspects of the topic?
- Do they make use of multiple tools discussed in the lesson? How much did they adapt the example code to fit their drawing’s goals?
- Are the methods being used deliberately and in order to support the purpose of the sketch? Or are they copying and pasting without much thought?
- Are the student’s questions specific to issues in their project? Or is it just ‘it’s not working’?

Are the students using their creative and visual communication skills?
- How many different techniques or combination of tools did they use before settling on an idea? Or did they stop at the first idea they came up with?
- Did the student extend themself by looking at tools beyond the demonstration?
- Is the student demonstrating a similar amount of care and attention to detail in their digital as well as physical drawings? 

How are the students keeping track of their personal and artistic growth?
- Was the student’s summary of their tool and drawings provide a clear and specific overview of their process?
- How did the student articulate the difference between the digital and physical drawing processes?
- How did the student manage frustration or challenges throughout the process and how did they comment on these challenges after they were resolved?
