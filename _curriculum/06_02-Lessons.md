---
# This is the frontmatter
title: "A Walk in the Neighborhood" # Title and Heading 1
permalink: /walkInNeighborhood-lessons/2 # Give your page a permalink
published: true
---

## What is a Conditional Statement?

Conditional statements, or sometimes called conditional expressions, is a fundamental concept in programming that can be akin to a flow chart.

> From CodeAcademy:
> "Conditionals enable programs to make decisions and perform different actions depending on whether a condition is true or false and help with flow control.”

In this lesson, we’ll use conditional statements to control how a character walks around a map and reacts to reaching different locations. These skills will help you build your own interactive **Walk in the Neighborhood** prototype.

There are various kinds of conditional statements:

- If-then
- Else-if
- If-then-else

And we can use our operators (&&, ==, ||, < or >) in addition to it all!
✨ Understanding conditional statements will provide a foundational logic that we can continually use and come back to in mouse- and key-based interactions.

### 2A. If-then Statements

An if-then statement is essentially asking **if** (something is true), and **then** executing the { statements within the brackets }.

```js
if (test) {
    run statement;
}
```

If the “test” (as indicated by the parenthesis) is true, then execute the { statements within the brackets }.

An example might be

```js
if (my right arrow key is presed) {
  move my character to the right by 1 pixel.
}
```

First, to note, when we say keys — we’re referring to the keys on your computer or laptop’s keyboard. Not house keys, or piano keys. But, that’s not to say we couldn’t make our own custom alternative keyboards in future units! Every key on our computer keyboard is a programmed object — when we press the letter “a” key, it sends information to our computer to write down the letter “a” on our screen. But, we could re-program it to mean anything! And we’ll get into that shortly.

**Getting Ready for the Neighborhood Project:** Before we start building our actual Neighborhood projects, let's work on learning the coding concepts in a simple program where our "character" is an ellipse moving around on a blank canvas. Let's start writing the code to make our "character" move right when the RIGHT arrow key is pressed. We can do this by checking if the user is pressing the RIGHT arrow key -- and IF that is true, THEN move the position of the character to one pixel to the right (increment the x location of the character by one).

For now, we'll use a little circle as our character. Later, we'll style our uploaded images to take its place.

```jsx
let x = 100;
let y = 100;

function setup() {
  createCanvas(400, 300);
}

function draw() {
  background(200);
  ellipse(x, y, 40);

  if (key == RIGHT_ARROW) {
    x = x + 1;
  }
}
```

In this example, the character ONLY moves to the right if the RIGHT arrow key is pressed. But what happens if it's not pressed?

_The answer is: nothing._

There are no other instructions or statements in our code examples. All the computer is looking for is **if** the test is true, **then** we run the statement. So, we might want to add an “**else**” for some more complexity.

### 2B. If-Then-Else Statements - Directional Appearance

An if-then statement executes what is true, but adding an “else” then offers another set of instructions in the case that the first test isn’t met.

```jsx
if (test) {
    statement 1;
} else {
    statement 2;
}
```

How might this look in the Neighborhood project? In the code below, it is telling the computer to check if my character is moving right. If that's true, my character to change color to red. Otherwise (else), stay gray.

```jsx
if (my character is moving right) {
    my character is red;
} else {
    My character is blue;
}
```

How might this look with our ellipse character?

```js
let x = 100;
let y = 100;

function setup() {
  createCanvas(400, 300);
}

function draw() {
  background(200);
  ellipse(x, y, 40);

  if (key == RIGHT_ARROW) {
    fill(255, 0, 0); //right arrow = red
    x = x + 1;
  } else {
    fill(150); // any other key = gray
  }
}
```

### 2C. Nested If-Statements

p5.js has a built in boolean variable called `keyIsPressed.` This variable tests if a key on your keyboard is pressed, and IF that is true, THEN do something. The above example is just checking if the RIGHT arrow key is pressed, but if we want to check if multiple keys are pressed, we will have to nest those if-statements under the `keyIsPressed` function.

Check it out:

```js
let x = 100;
let y = 100;

function setup() {
  createCanvas(400, 300);
}

function draw() {
  background(200);

  if (keyIsPressed) {
    if (key == RIGHT_ARROW) {
      fill(255, 0, 0); // right-facing = red
      x = x + 1;
    }
    if (key == LEFT_ARROW) {
      fill(0, 255, 0); // left-facing = green
      x = x - 1;
    }
    if (key == UP_ARROW) {
      fill(255, 255, 0); // up-facing = yellow
      y = y - 1;
    }
    if (key == DOWN_ARROW) {
      fill(0, 0, 255); // down-facing = blue
      y = y + 1;
    }
  } else {
    fill(150); // standing still = gray
  }

  ellipse(x, y, 40);
}
```

**Step-by-Step Explanation**

```js
if (keyIsPressed) {
```

- This checks whether **any key** is being pressed.
- If yes, the code inside the {} runs.
- if no, the program skips to the `else` and fills the ellipse with gray `(fill(150))`.

Inside that block of code, we have nested `if` statements:

```js
if (key == RIGHT_ARROW) {
  fill(255, 0, 0);
  x = x + 1;
}
```

- This checks if the specific key being pressed is the **right arrow**
- If so, it sets the fill color to red and moces the ellipse right by adding 1 to `x`.

```js
if (key == LEFT_ARROW) {
  fill(0, 255, 0);
  x = x - 1;
}
```

- If the key is the **left arrow**, it sets the color to green an dmoces the ellipse left.
- So on and so forth for the up and down arrows.

##### What does "nested" mean here?

These `if` statements are called nested because they are all inside the outer `if(keyIsPressed)` block.

- That outer `if` acts like a gate: none of the movement or color logic will run unless a key is pressed.
- So the nested `if`s only get evaluated if `keyIsPressed` is true.

Now we're ready to build out **Walk in the Neighborhood** Project!
