---
# This is the frontmatter
title: "A Walk in the Neighborhood" # Title and Heading 1
permalink: /walkInNeighborhood-lessons/ # Give your page a permalink
published: true

---

```jsx
let x = 25;
let h = 20;
let y = 25;
function setup() {
  createCanvas(480, 120);
}
function draw() {
  background(204);
  rect(x, y, 300, h);        // Top
  x = x + 100;
  rect(x, y + h, 300, h);    // Middle
  x = x - 250;
  rect(x, y + h*2, 300, h);  // Bottom
}
```

### Updating a value
We can also update the value of a variable throughout our code. It can mean one value in a specific context, and then change its value in another.

- Replacing the value of a variable
    - Variables can update themselves with new information - ie. x = x+1; This means that x will keep updating to add 1 to itself.
    - If using “let,” we can change the variable type. The same variable used for storing numbers can also update to be text or array of values.
    
# Lesson Plans & Technical Steps
## 1. Variables + Animation
![Animating with p5.js]({{ "/assets/images/curriculum/Unit-5_Sample-2.gif" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/SwhyQV9_v) 

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
  console.log("current frame: " + frameCount); // frameCount is a p5.js variable that shows the number of frames that have elapsed since the canvas loaded
  
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

## 2. What is a Conditional Statement?

Conditional statements, or sometimes called conditional expressions, is a fundamental concept in programming that can be akin to a flow chart. From CodeAcademy, conditionals “enable programs to make decisions and perform different actions depending on whether a condition is true or false and help with flow control.”

There are various kinds of conditional statements:

- If-then
- Else-if
- If-then-else

And we can use our operators (&&, ==, ||, < or >) in addition to it all! 
✨ Understanding conditional statements will provide a foundational logic that we can continually use and come back to in mouse- and key-based interactions.



### 2A. If-then Statements

An if-then statement is essentially asking **if** (something is true), and **then** executing the { statements within the brackets }. 

```jsx
if (test) {
    run statement;
}
```

If our test “You like pizza” is true; then we’ll order a pizza!  
We might write this in pseudo-code as:

```jsx
if (You like pizza) {
    We order pizza;
}
```

If the “test” (as indicated by the parenthesis) is true, then execute the { statements within the brackets }.

**🎨 In our Drawing Tool:** We need to start with adding circles to the canvas wherever the mouse is pressed. We can do that by using a special p5.js boolean variable called “mouseIsPressed.” This variable tests if the mouse is pressed — and IF it is true (that the mouse is pressed), THEN { draw a circle a the x and y position of where my mouse’s x and y position is }. 

```jsx
function draw(){
    if (mouseIsPressed) {  // If the mouseIsPressed is (==) true
	    circle(mouseX, mouseY, mW);  // Then draw a circle where mouseX and mouseY is, and the diameter of the circle is mW                     
    }
}
```

In our previous example, we ONLY order the pizza if it is true that we like pizza. But what happens if we don’t like pizza (*gasp*) or if we pressed any other key? 

*The answer is: nothing.* 

There are no other instructions or statements in our code examples. All the computer is looking for is **if** the test is true, **then** we run the statement. So, we might want to add an “**else**” for some more complexity. 

### 2B. If-Then-Else Statements

An if-then statement executes what is true, but adding an “else” then offers another set of instructions in the case that the first test isn’t met. 

```jsx
if (test) {
    statement 1;
} else {
    statement 2;
}
```

Let’s revisit our pizza example. Now, if you like pizza, we will order pizza. But if you DON’T like pizza, we’ll order spaghetti. 

```jsx
if (You like pizza) {
    We order pizza;
} else {
    We order spaghetti;
}
```

The “else” offers us the ability to execute another function if we respond with “anything ELSE” than what the initial test was asking for. So, it may be the case that I don’t like spaghetti either. But as long as you DON’T like pizza, and irregardless if you like spaghetti, you’ll end up with spaghetti anyway. All the “else” looks for is if your input was “anything ELSE” than what needs to be true. 

**🎨  In our Drawing Tool:** We might want to add different interactions based on the keys pressed on the keyboard. We’ll talk more about it in Lesson 2: Key interactions. If you check out our code example, we’re drawing circles. But here’s a way we can change the color of circles based on if we press the letter key “r” vs. another key. 

```jsx
function keyPressed() { // We're going to add our if-then-else statement inside the keyPressed function. So whenever a key is pressed:

  if (key == "r") { // The program will check if key pressed is "r" 
    fill(255,0,0);  // If YES, the key pressed is "r" -- then fill the color as Red
  } else {
	  fill(255);  // If the key pressed is anything ELSE -- then fill the color as White
  }
  
}
```

### 2C. Else-if Statements

Not to be confused with an “else” but this is adding both “else” and “if” together: an **“else-if”**

In our earlier example, all that our statements looked for was whether or not we liked pizza. And it offered us one of two options: we’d either end up with pizza or spaghetti. Adding the Else-if statements gives us the option for more specificity in the form of adding more tests. 

```jsx
if (test 1) {
    statement 1;
} else if (test 2) {
    statement 2;
}
```

```jsx
if (You like pizza) {
    We order pizza;
} else if (You like spaghetti) {
    We order spaghetti;
}
```

And we can add an else to the mix: 

```jsx
if (You like pizza) {
    We order pizza;
} else if (You like spaghetti) {
    We order spaghetti;
} else {
    We'll look at delivery services;
}
```

### 2D. Controlling Animations with If/Else Statements
![Animating with p5.js]({{ "/assets/images/curriculum/Unit-5_Sample-3.gif" | relative_url }})  
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


### Something to note:

- We can have as many if-then statements as we want, but they’d be separate
- We can attach on as many “else-if” to our “if-then” statements as we need
- We can only have one “else” at the end, because it’s saying if it’s “anything ELSE” other than what was tested for, run this statement. “else” acts as a catch-all, so we couldn’t have more than one “else” in one if-then group at a time

### Practice

**Start here (Easy)**

How can we add another color to the program?

- 🙋 *Answer*
    
    Continuing our examples of Else-if Statements, we can keep adding different keys to create new colors:
    
    ```jsx
    function setup() {
      createCanvas(400, 400);
      background(0);
      fill(255);
      text("press r,g,b, or x to change color", 10, 25);
    }
    
    function draw() {
      if (mouseIsPressed) {
        circle(mouseX, mouseY, 50);
      }
    }
    
    function keyPressed() {
      if (key == "r") {
        fill(255, 0, 0);
      } else if (key == "g") {
        fill(0, 255, 0);
      } else if (key == "b") {
        fill(0, 0, 255);
      } else if (key == "x") {
        // similarly you can keep adding keys to the else-if statement
        fill(random(255), random(255), random(255)); // in this case, pressing "x" changes the brush color to a random color
      } else {
        fill(255);
      }
    }
    ```
    

**Level up (Medium)**

How can we change the size of the brush to get bigger? smaller?

- 🙋 *Answer*
    
    We can create a variable to store an initial default value (brushSize = 10;), and then if the user pressed “n” or “m” the variable “brushSize” add +1 or subtract -1 to the value to make the size larger or smaller respectively. 
    
    ```jsx
    let brushSize = 10;
    
    function setup() {
      createCanvas(400, 400);
      background(0);
      fill(255);
      text("Welcome to my drawing tool!", 10, 25);
      text("Press r,g,b, or x to change color.", 10, 50);
      text("Press n or m to change brush size.", 10, 75);
    }
    
    function draw() {
      if (mouseIsPressed) {
        circle(mouseX, mouseY, brushSize);
      }
    
      if (keyIsPressed) {
        if (key == "n") {
          brushSize = brushSize + 1;
          console.log("bigger");
        } else if (key == "m") {
          brushSize = brushSize - 1;
          console.log("smaller");
        }
      }
    }
    
    function keyPressed() {
      if (key == "r") {
        fill(255, 0, 0);
      } else if (key == "g") {
        fill(0, 255, 0);
      } else if (key == "b") {
        fill(0, 0, 255);
      } else if (key == "x") {
        // similarly you can keep adding keys to the else-if statement
        fill(random(255), random(255), random(255)); // in this case, pressing "x" changes the brush color to a random color
      } else {
        fill(255);
      }
    }
    
    ```
    

**Extra push (Hard)**

How can we change the shapes into an image?  

- 🙋 *Answer*
    
    Recall our earlier Unit 1 examples on how to add an image (declare a variable, load the image in Preload, and call it using the image() function). Using our if-then statements and mouseIsPressed boolean, we can create a drawing brush using an image. 
    
    ```jsx
    let img;
    
    function preload(){
      img = loadImage("https://png.pngtree.com/png-vector/20220411/ourmid/pngtree-red-3d-heart-emoji-realistic-shadow-png-image_4539964.png");
    }
    
    function setup() {
      createCanvas(400, 400);
      background(0);
      imageMode(CENTER);
    }
    
    function draw() {
      if (mouseIsPressed) {
        image(img,mouseX,mouseY,100,100);
      }
    }
    ```
    

### Prompts

1. When do we use “if-then” statements in our daily lives? Can you map it out in a flow chart? 
2. In our examples, we used “if-then” statements for selecting colors: what else could we use the “if-then” statement for in a drawing program?

## 3. Key interactions

Now, we’ve learned the basics of conditional statements and tried mouse interactions. We can look at the similarities and transfer the knowledge from mouse interactions to key interactions. And furthermore, combining our knowledge of conditionals, we can use specific keys to unlock new potential interactions! 

First, to note, when we say *keys* — we’re referring to the keys on your computer or laptop’s keyboard. Not house keys, or piano keys. But, that’s not to say we couldn’t make our own custom alternative keyboards in future units! Every key on our computer keyboard is a programmed object — when we press the letter “a” key, it sends information to our computer to write down the letter “a” on our screen. But, we could re-program it to mean anything! And we’ll get into that shortly. 

Similarly to the mouse interactions, p5.js offers various key interactions with functions, booleans and special variables!

Here are some fun ones to know:

- keyIsPressed
    - This is a boolean-type of variable.
    - KeyIsPressed is checking for: is any key pressed? Yes or No?
- keyCode or key
    - This might be helpful to add inside your keyIsPressed, because keyIsPressed is looking is ANY key being pressed? If so, then you can use keyCode or key to verify if it’s a specific key.
    - Key codes are:
        - A number system variable
        - keyCode is looking for a specific number, each key on your keyboard is connected to a universal number that is used in a variety of industries!
        - You can look up tables online for Key Codes.
        - For example: the “a” key is keyCode 65.
    - Key:
        - A string system variable
        - Key is looking for an actual letter, or what we call a string.
        - For example: the “a” is “a”
- keyPressed()
    - A function that sets a code block to run once automatically when the user presses any key
    - [https://p5js.org/reference/#/p5/keyPressed](https://p5js.org/reference/#/p5/keyPressed)
- keyIsDown()
    - Returns true if the key it’s checking is pressed and false if not.
    - keyIsDown() is helpful when checking for multiple different key presses. For example, keyIsDown()can be used to check if both LEFT_ARROW and UP_ARROW are pressed
    - [https://p5js.org/reference/#/p5/keyIsDown](https://p5js.org/reference/#/p5/keyIsDown)

**🎨  In our Drawing Tool:** Let’s re-review our earlier example in the Lesson 2: Conditionals. 

```jsx
function keyPressed() { // When the key is pressed

  if (key == "r") {  // And if the key is "r" , fill the circle with red 
    fill(255,0,0);
  } else if (key == "g") {  // Otherwise, if the key is "g" , fill the circle with green 
    fill(0,255,0); 
  } else if (key == "b"){   // Otherwise, if the key is "b" , fill the circle with blue 
    fill(0,0,255);
  } else if (key == "x") {  // Otherwise, if the key is "x" , fill the circle with black 
    fill(0,0,0);
  } else {      // And, if the key pressed is anything else other than r, g, b, or x, fill the circle with white 
	  fill(255);
	  
}
```

Here, we’re using a function called keyPressed — which is telling p5.js that any time I press any key on the keyboard, run the code { inside the brackets }.

But since we want things to happen, to not just any key, but specific keys to have specific actions — we use our conditionals. 

In our drawing tool, we use the “key” variable which stores the **string** of your last typed letter. And we’re evaluating that with an if-then statement: is the last type letter an “r”? if not, is it a “g”? if not, is it a “b”? and so forth. And if it is one of those things, we run the code { inside it’s brackets }. 

### Practice

**Start here (Easy)**

How can I change the background color or “refresh” when a specific key is pressed? 

- 🙋 *Answer*
    
    Just like using the Else-if statements as usual, we’ll utilize the background(0); statement to draw over a new background. 
    
    ```jsx
    let brushSize = 10;
    
    function setup() {
      createCanvas(600, 600);
      background(0);
      fill(255);
      text("Welcome to my drawing tool!", 10, 25);
      text("Press r,g,b, or x to change color.", 10, 50);
      text("Press n or m to change brush size.", 10, 75);
      text("Press 0 to refresh the page.", 10, 100);
    }
    
    function draw() {
      if (mouseIsPressed) {
        circle(mouseX, mouseY, brushSize);
      }
    
      if (keyIsPressed) {
        if (key == "n") {
          brushSize = brushSize + 1;
          console.log("bigger");
        } else if (key == "m") {
          brushSize = brushSize - 1;
          console.log("smaller");
        }
      }
    }
    
    function keyPressed() {
      if (key == "r") {
        fill(255, 0, 0);
      } else if (key == "g") {
        fill(0, 255, 0);
      } else if (key == "b") {
        fill(0, 0, 255);
      } else if (key == "x") {
        fill(random(255), random(255), random(255));
      } else if (key == 0) {
        background(0); // if the key is 0, we'll "reset" by drawing another background on top of the image 
      } else {
        fill(255);
      }
    }
    
    ```