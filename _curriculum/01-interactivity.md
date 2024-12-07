---
# This is the frontmatter
title: "Digital Drawing: Interactive Art" # Title and Heading 1
permalink: /1-interactivity/ # Give your page a permalink
published: false

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

## Lesson Plan 1: Mouse interactions

### Mouse Special Variables

- mouseX == this variable always assigns the current X position of your cursor
- mouseY == this variable always assigns the current Y position of your cursor

**🎨  In our Drawing Tool:** 

```jsx
function draw(){

		circle(mouseX, mouseY, mW);  // saying draw a circle. The circle’s position (x,y) is wherever the mouse’s / cursor’s  X + Y is!

}
```

So, now the circle is following our every cursor’s move. But why is it that for some folks it might be tracking the mouse vs. some it’s actually drawing? Try it out!

**Circle FOLLOWS mouse:**

```jsx
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(mouseX,mouseY, 50);
}
```

**Circle DRAWS on canvas:**

```jsx
function setup() {
  createCanvas(400, 400);
  background(220);
}

function draw() {
  ellipse(mouseX,mouseY, 50);
}
```

Let’s return to our original question: Why is in one the circle is following the mouse vs. some it’s actually drawing?

- 🙋*Answer*
    
    Remember, the code runs in order! Check out where background() is. If it’s in setup(), then background only draws once! But if it’s inside draw() then your background keeps drawing on top of your circle, which gives the illusion that it’s only tracking instead of drawing.
    

### Booleans: Mouse Is Pressed?

[https://p5js.org/reference/#group-Events](https://p5js.org/reference/#group-Events)

Remember variables? mouseIsPressed == is a boolean. A boolean is a variable that can either hold the value of “true” or “false”.  So mouseIsPressed is a variable that is looking for if the mouse is pressed or not. Think of it as asking: is the mouse pressed? Y or N?

So, have you noticed how in the earlier example, the circles just automatically start drawing? What if we ONLY want it to draw when the mouse is pressed?

**🎨  In our Drawing Tool:** 

```jsx
function draw(){

		if (mouseIsPressed) {

				circle(mouseX, mouseY, mW);

		}

}
```

It’s saying, if “mouseIsPressed == true” or in other words,” is the mouse pressed? Yes!” – then complete the actions or code inside the { brackets }. 

Now, we can move our mouse freely without the circle drawing. And only when the mouse is pressed, will it create a circle wherever the mouse x and y positions are, at the size of “mW” and filled with the color we set as “r,g,b”. We will discuss this more in Lesson 3: Conditionals.

In mouseIsPressed (examples above), this is a type of variable called a boolean which can only store one of two values. But there are some other exciting things we can use, like functions! Let’s check them out in the next section.

### Mouse-related Functions

Functions are events or actions that p5.js is aware of, much like draw() or setup(). They are formatted a little differently from how we’ve been writing things before.  

- mousePressed() { // code runs automatically when the user presses a mouse button  }
- mouseDragged() { //  code runs automatically when the mouse moves while a button is pressed (click and drag mouse) }
- mouseReleased() { // code runs automatically when the user releases a mouse button after having pressed it (so it won’t run on press, only after you release after pressing) }
- mouseClicked() {  // gosh, this is tricky but its a “click” the action of a mouse being pressed and released :) haha }

What?! This is the super exciting thing about code and math; there are so many ways to solve the same “problem.”

Instead of using a boolean inside of draw, we can use the mousePressed() function. p5.js now knows that whatever code you put inside the { brackets } of mousePressed() it will run it, when the mouse gets Pressed.

**🎨  In our Drawing Tool:** 

```jsx
function setup() {

createCanvas(400, 400);

}

function draw() {

}

function mousePressed() {

		ellipse(mouseX,mouseY, 50);

}
```

Important note: did you realize how it doesn’t draw the same way? This is because the code only runs once, when the mouse presses –  think of an on and off switch. If you wanted to keep it going, you might use something like mouseDragged().

```jsx

function setup() {
  createCanvas(400, 400);
}

function draw() {
}

function mouseDragged() {
  ellipse(mouseX,mouseY, 50);
}

```

### Prompts

1. What is the difference between a Function (ie. mousePressed) and a Boolean (ie. mouseIsPressed)? And what does the interaction or output look like: how are they similar? how are they different? 
2. What are the ways we’ve used mouseX and mouseY in this session? How else might we use mouseX and mouseY? (Consider other games: Pong, Lilo & Stitch Sandwich Stacker games) 
3. What might you use a mouse interaction for? Can you list a few ideas? 

---

## Lesson Plan 2: Conditional Statements

### What is a Conditional Statement?

Conditional statements, or sometimes called conditional expressions, is a fundamental concept in programming that can be akin to a sort of flow chart. From CodeAcademy, conditionals “enable programs to make decisions and perform different actions depending on whether a condition is true or false and help with flow control.”

There are various kinds of conditional statements:

- If-then
- Else-if
- If-then-else

And we can use our operators (&&, ==, ||, < or >) in addition to it all! 

**✨ Understanding conditional statements will provide a foundational logic that we can continually use and come back to in mouse- and key-based interactions.** 

### If-then Statements

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

**🎨 In our Drawing Tool:** We need to start with adding circles to the canvas wherever the mouse is pressed. We can do that by using a special p5 boolean variable called “mouseIsPressed.” We will talk more about mouse interactions in Lesson 2: Mouse interactions. This variable tests if the mouse is pressed — and IF it is true (that the mouse is pressed), THEN { draw a circle a the x and y position of where my mouse’s x and y position is }. 

```jsx
function draw(){
 
	  if (mouseIsPressed) {  // If the mouseIsPressed is (==) true
	    circle(mouseX, mouseY, mW);  // Then draw a circle where mouseX and mouseY is, and the diameter of the circle is mW 
	  }

}
```

In our previous examples, we ONLY order the pizza if it is true that we like pizza or “a” appears ONLY when the letter key “a” is pressed. But what happens if we don’t like pizza (*gasp*) or if we pressed any other key? 

*The answer is: nothing.* 

There are no other instructions or statements in our code examples. All the computer is looking for is **if** the test is true, **then** we run the statement. So, we might want to add an “**else**” for some more complexity. 

### If-Then-Else Statements

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

**🎨  In our Drawing Tool:** We might want to add different interactions based on the keys pressed on the keyboard. We’ll talk more about it in Lesson 3: Key interactions. If you check out our code example, we’re drawing circles. But  Here’s a way we can change the color of the circles based on if we press the letter key “r” vs. another key. 

```jsx
function keyPressed() { // We're going to add our if-then-else statement inside the keyPressed function. So whenever a key is pressed:

  if (key == "r") { // The program will check if key pressed is "r" 
    fill(255,0,0);  // If YES, the key pressed is "r" -- then fill the color as Red
  } else {
	  fill(255);  // If the key pressed is anything ELSE -- then fill the color as White
  }
  
}
```

### Else-if Statements

Not to be confused with an “else” but this is adding BOTH and words  “else” AND “if” together: an “else-if”

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

**🎨  In our Drawing Tool:** We’ve made color changes for one key, but now we can assign different colors to different keys! Woo hoo~ Read the comments below to see how we’ve added to our initial If-Then-Else statement by adding Else-if. 

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
```

### Something to note:

- We can have as many if-then statements as we want, but they’d be separate
- We can attach on as many “else-if” to our “if-then” statements as we need
- We can only have one “else” at the end, because it’s saying if it’s “anything ELSE” other than what was tested for, run this statement. “else” acts as a catch-all, so we couldn’t have more than one “else” in one if-then group at a time.


### Prompts

1. When do we use “if-then” statements in our daily lives? Have you negotiated anything, or concocted a plan with someone where you’ll follow through with a plan IF someone occurs, and a back-up plan (”if-then-else”) had it not. Can you map it out in a flow chart? 
2. In our examples, we used “if-then” statements for selecting colors: what else could we use the “if-then” statement for in a drawing program?

---

## Lesson Plan 3: Key interactions

Now, we’ve learned the basics of conditional statements and tried mouse interactions. We can look at the similarities and transfer the knowledge from mouse interactions to key interactions. And furthermore, combining our knowledge of conditionals, we can use specific keys to unlock new potential interactions! 

First, to note, when we say keys — we’re referring to the keys on your computer or laptop’s keyboard. Not house keys, or piano keys. But, that’s not to say we couldn’t make our own custom alternative keyboards in the future 😉 Every key on our computer keyboard is a programmed object — when we press the letter “a” key, it sends information to our computer to write down the letter “a” on our screen. But, we could re-program it to mean anything! And we’ll get into that shortly. 

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

```wasm
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


### Prompts

1. We references Key Codes. Can you spell your name with Key Codes, using an existing Key Code table? 
    1. Why might we use Key Codes as opposed to keys in some instances? 
2. What is the difference between a Function (ie. keyPressed) and the Variable (ie. key)? 
3. What might you use a key interaction for? Can you list a few ideas?  

---

## Assessments

As an educator and facilitator, we’re looking for a thorough understanding of:

- Logics within conditional statements
    - Can the student map out a flow chart of how their code will function? (Start with paper and pen, and draw out what the flow chart might look like, ie. pseudocode)
    - Can the student properly interpret the differences between an If-then, If-then-else, and Else-if?
- Mouse functions vs. Key functions
    - Can the student recognize how the Mouse interactions differ from the Key interactions? What are the affordances of using a key vs. a mouse in different instances (ie. a mouse is best used for drawing, whereas a key can be used for options). And also identify their similarities in the logic?
- Interactivity in the arts
    - Can the student integrate a form of interaction (inviting the user to click, press a key) to generate a new, richer, or unique meaning and perspective in an art piece?
