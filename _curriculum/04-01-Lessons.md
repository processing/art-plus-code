---
# This is the frontmatter
title: "Mask Generator" # Title and Heading 1
permalink: /maskGenerator-lessons/1 # Give your page a permalink
published: true
---

Mask Generator remixes Critical Computation by Xin Xin and Katherine Moriwaki, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en)

## Variables

### Grade 6~8

#### What is a Variable?

A variable is a container used to store data. Picture a box that lets you store data. 

But what do we mean by data? These data can be numbers:

 ![Variable box that stores numbers]({{ "/assets/images/curriculum/Unit-2_Sample-3.png" | relative_url }})

Or words:

 ![Variable box that stores numbers]({{ "/assets/images/curriculum/Unit-2_Sample-4.png" | relative_url }})

Or your favorite images and songs:

 ![Variable box that stores numbers]({{ "/assets/images/curriculum/Unit-2_Sample-5.png" | relative_url }})

 We store data in these boxes so that they can be used as resources while a computer program is running. 

#### Creating a Variable

In order to create a variable, we need to give the variable a name. Think of this as the label you will be taping on the box to remind yourself what you've put inside the box. 

 ![Variable box labeled tomatoes]({{ "/assets/images/curriculum/Unit-2_Sample-1.png" | relative_url }}) 

If we want to indicate that there are 3 items inside the `tomatoes` box, we would write it out like this:

```js
let tomatoes = 3; // assign 3 to the tomatoes variable

function setup() {
  createCanvas(400, 400);
  console.log(tomatoes); // load tomatoes variable
}
```

**Tip:** Conventionally, the first letter of a variable name is written in lower-case.
{: .notice--success}

There are some funny things here. First, we're using a new word called `let`. What is `let`? You can think of `let` like a magic spell that lets us create variable to store data. 

> **🧠Teacher Trick:**
> Think of yourself as creating a new world, declaring aloud **let** there be light! 
> By declaring with “let”, we’re proclaiming something (a variable) into existence in our world of code. 

We're also using another JavaScript feature called `console.log()` to load the content of our `tomatoes` variable. `console.log()` helps us to keep track of what's inside a variable and debug code. We will be using it a lot to complete this project. 

Also, `let tomatoes = 3;` is being written above `function setup()`! That's right. Think about the computer program like a factory assembly line, and you need to have all of your boxes lined up before loading them into the machines. 

**Tip:** By default, you will be creating variables at the top of your program. Variables that are created outside of `function setup()` and `function draw()` are called global variables.
{: .notice--success}

Let's practice using variables by remixing the [lollipop example](https://editor.p5js.org/xinemata/sketches/reojWdPOp). Create variables that would store all the numbers we used to draw the lollipop: 

```js
// Lollipop stick variables
let stickX = 200;
let stickY = 240;
let stickWidth = 10;
let stickHeight = 100;
// Lollipop candy variables
let candyX = 200;
let candyY = 200;
let candyWidth = 60;
let candyHeight = 60;

function setup() {
  createCanvas(400, 400);
  noStroke();
  rectMode(CENTER);
}

function draw() {
  background(220);

  //Lollipop stick
  fill(255);
  rect(stickX, stickY, stickWidth, stickHeight);

  //Lollipop candy
  fill(180, 29, 159);
  ellipse(candyX, candyY, candyWidth, candyHeight);
}
```
When you click the play button, you should see the exact same lollipop sketch appearing in front of you. But instead of seeing a bunch of random numbers on the screen, we now have a better idea of what each number was created for. Amazing!

**Tip:** When a variable name contains two words, there are two conventional ways to format the text. The first way, also known as camel case, capitalizes the second word, e.g. `candyWidth`. The second way, also known as snake case, uses an underscore symbol to connect the two words, e.g. `candy_x`.
{: .notice--success}

##### Applying Arithmetic to Variables

You can apply arithmetic operators such as +, -, *, and / to variables! The following example shows how you can draw three circles with equal spacing in between:

```js
let x = 200;
let y = 200;
let d = 80;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(x - 100, y, d, d); // left
  ellipse(x, y, d, d); // middle
  ellipse(x + 100, y, d, d); // right
}
```

Revisiting the [multiple rect() example](https://editor.p5js.org/xinemata/sketches/gWHc2OalC), where we were supposed to draw a row of rectangles diagonally across the screen, we could apply arithmetic to achieve the effect. 


```js
let offset = 40; 
let boxD = 40;

function setup() {  
  createCanvas(400, 400); // w, h
}

function draw() { 
  background(220); 
  rect(offset*0, offset*0, boxD, boxD); // x, y, w, h
  rect(offset*1, offset*1, boxD, boxD); // x, y, w, h
  rect(offset*2, offset*2, boxD, boxD); // x, y, w, h
  rect(offset*3, offset*3, boxD, boxD); // x, y, w, h
  rect(offset*4, offset*4, boxD, boxD); // x, y, w, h
  rect(offset*5, offset*5, boxD, boxD); // x, y, w, h
  rect(offset*6, offset*6, boxD, boxD); // x, y, w, h
  rect(offset*7, offset*7, boxD, boxD); // x, y, w, h
  rect(offset*8, offset*8, boxD, boxD); // x, y, w, h
  rect(offset*9, offset*9, boxD, boxD); // x, y, w, h
}
```

 ![Two diagonal lines]({{ "/assets/images/curriculum/Unit-2_Sample-8.png" | relative_url }}) 

#### System Variables

The [p5.js contributors](https://github.com/processing/p5.js?tab=readme-ov-file#contributors) have created a couple of variables that are available for us to load and use. These system variables were created to bring joy and ease to the coding process. We will spend the rest of Art + Code to try them out.

##### mouseX and mouseY

The `mouseX` and `mouseY` variables load the X and Y positions of your cursor in real time, allowing you to interact with your drawing with your mouse. 

```js
function draw() {
  background(220);
  ellipse(mouseX, mouseY, 20, 20); // x, y, w, h
  console.log(mouseX, mouseY); // displays mouseX and mouseY values in real time
}
```
Aside from using `mouseX` and `mouseY` to control the X and Y positions of an ellipse, we can also use those real time inputs to control the size of the ellipse: 

```js
function draw() {
  background(220);
  ellipse(200, 200, mouseX, mouseY); // x, y, w, h
  console.log(mouseX, mouseY); // displays mouseX and mouseY values in real time
}
```
Or the color of the ellipse:

```js
function draw() {
  background(220);
  fill(mouseX, 100, 100); // r, g, b
  ellipse(mouseX, mouseY, 20, 20); // x, y, w, h
}
```

**Tip:** Similar to animation or a flip book, the modern browser has a framerate and refreshes 60 times per second! This illusion of real time can be interrupted when your browser slows down or crashes. 
{: .notice--success}

##### width and height

`width` and `height` variables loads the values of your canvas width and height, making it incredibly convenient to draw a shape in relation to the canvas. For example, if you'd like to draw two diagonal [line()](https://p5js.org/reference/p5/line/) across the canvas:

```js
function draw() {
  background(204);
  line(0, 0, width, height); // x1, y1, x2, y2
  line(width, 0, 0, height); // x1, y1, x2, y2
}
```

 ![Two diagonal lines]({{ "/assets/images/curriculum/Unit-2_Sample-6.png" | relative_url }}) 

 Or if you'd like to lay out your shapes with equal spaces in between: 

 ```js
 let dieR = 60;

function setup() {
  createCanvas(400, 400);
  noStroke();
}

function draw() {
  background(227, 47, 2);
  fill(245, 237, 220);
  ellipse(width / 2, height / 2, dieR, dieR); // places the pip in the center
  ellipse(width / 4, height / 4, dieR, dieR); // places the pip in the upper left corner
  ellipse((width / 4) * 3, height / 4, dieR, dieR); // places the pip in the upper right corner
  ellipse(width / 4, (height / 4) * 3, dieR, dieR); // places the pip in the lower left corner
  ellipse((width / 4) * 3, (height / 4) * 3, dieR, dieR);
  // places the pip in the lower right corner
}
 ```
 ![A red die]({{ "/assets/images/curriculum/Unit-2_Sample-7.png" | relative_url }}) 