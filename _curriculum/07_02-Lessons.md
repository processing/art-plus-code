---
# This is the frontmatter
title: "Observing Patterns" # Title and Heading 1
permalink: /patterns-steps/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/curriculum/Unit-7_Practice-1.png
    image_path: /assets/images/curriculum/Unit-7_Practice-1.png
    alt: "thin horizontal rectangles transitioning from blue to pink"
    title: "Loops Pracitce #1"
  - url: /assets/images/curriculum/Unit-7_Practice-2.png
    image_path: /assets/images/curriculum/Unit-7_Practice-2.png
    alt: "criss crossed white lines on a red background"
    title: "Loops Pracitce #2"
  - url: /assets/images/curriculum/Unit-7_Practice-3.png
    image_path: /assets/images/curriculum/Unit-7_Practice-3.png
    alt: "a circular gradient going from dark navy out to white"
    title: "Loops Pracitce #2"

---

# Lesson Plans & Technical Steps

## 1: Iteration
![Starting off with loops]({{ "/assets/images/curriculum/Unit-7_Sample-2.png" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/eDdQWe8XG) 

*If you have the Auto-refresh box checked while working in the P5JS editor, it might be a good idea to uncheck the box as loop errors (like infinite loops) can crash the page.*

Let’s say that we want to draw a striped pattern in P5JS. To do so, we will probably need to draw a rectangle multiple times at regular intervals. The code will probably look like this:
```js
rect(0, 20, 5, 100);
rect(10, 20, 5, 100);
rect(20, 20, 5, 100);
rect(30, 20, 5, 100);
rect(40, 20, 5, 100);
rect(50, 20, 5, 100);
```

If we only need to draw a small handful of rectangles, writing multiple lines like this would probably not be a manageable task. But what if we needed 100 lines? Or, what if we decide later that we want all of the rectangles to be longer or further spaced apart? The task then quickly becomes extremely tedious and unreasonable, not to mention making our code clunky with more lines than necessary.

Taking a closer look at the lines of code above, we can see that they are all nearly identical except for one number in the command, specifically the x-position value. We can also see that the value of the x-position increases at a regular interval. The above code could also be written like so:
```js
let i = 0;

rect(i, 20, 5, 100);
rect(i + 10, 20, 5, 100);
rect(i + 20, 20, 5, 100); // or, i + 10 + 10
rect(i + 30, 20, 5, 100); // or i + 10 + 10 + 10
rect(i + 40, 20, 5, 100);
rect(i + 50, 20, 5, 100);
```

We can achieve a regular pattern by using a counter variable and adding the same amount to it every time we draw another shape. Programmers often use i for this variable, short for index.

This kind of logic can be condensed into a **for loop**. A typical for loop looks like this: 
```js
for (let i = 0; i < 200; i = i + 10) {
  rect(i, 20, 5, 100);
}
```

You can see that the variable i is being used here to create the repeating pattern. The statements between the semi-colons between the parentheses after the keyword for dictate how the iteration happens:
```js
for (/* INITIALIZATION */; /* CONDITION / ; /* INCREMENT or DECREMENT */) {
  /* the code between the curly brackets will repeat 
  according to what is dictated in between the parentheses */
}
```

**Initialization:**
Before the first semi-colon, create a new variable and set a value. This value is the starting point for the loop. In the example above, the counter variable is i, and the initial value is 0. Use the same syntax as when creating other variables:
```js
let i = 0;
let w = 1;
let r = 400;
```

**Condition:**
In the middle section, use a boolean expression to set an end condition. As long as the boolean statement between the two semi-colons evaluates to *TRUE*, the loop will repeat. In the example above, as long as the value of i is less than 100, the loop will repeat. Once the value of i exceeds 100, the loop will stop: 
```js
i < 200 // as long as the value of i is 100 or less, the loop will repeat
w === 10
l >= 80
```

**Increment or Decrement:**
The last section dictates how much the counter variable should change. Each time the for loop iterates, the counter variable will change by this amount. The syntax for this will use an arithmetic expression:
```js
i = i + 10 // add 10 to i everytime the loop repeats
w++ // this is shorthand for w = w + 1, or add one to w everytime the loop repeats
r -= 7 // this is shorthand for x = x - 7
```

Once the loop is set up, or we have set the rules for repetition, we just need to plug the counter variable into our code:
```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  for (let i = 0; i < 200; i = i + 10) {
    noStroke();
    fill(255, 166, 237);
    rect(i, 20, 5, 100);
  }
  for (let w = 1; w === 10; w++) {
    console.log(w)
  }
  for (let l = 400; l >= 80; l -= 7) {
    stroke(61, 140, 18);
    strokeWeight(2);
    line(10, l, 390, l);
  }
}
```


## 2: Making the Counter Variable Multi-task
![Getting comfortable with loops]({{ "/assets/images/curriculum/Unit-7_Sample-3.png" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/KmP0J0Ek_) 

When using for loops, there are a few different ways that the counter variable can be manipulated. These can be especially useful in an environment like P5JS when the loop is tied to a specific design. 

Some ways that we can extend the usefulness of the counter variable include…

Applying arithmetic expressions so that we can use the same counter variable for different purposes within a single for loop. Here, we are using the variable for both color and x-position:
```js
for (let i = 0; i <= 20; i++) {
    fill(255, 157, i * 20);
    rect(i * 30, 100, 10, 40);
}
```

Incorporating if/else statements. Using the modulo operator % is useful for setting intervals. Here, we are using the if statement with the modulo operator to make every other rectangle in a line a different color:
```js
for (let i = 0; i <= 20; i++) {
    if (i % 2 === 0) {
      fill(255, 255, 255);
    } else {
      fill(255, 0, 102);
    }
    
    rect(i * 20, 200, 10, 40);
}
```

Try these puzzles for practicing loops! 
*Hint: It can help to sketch out the pattern on a sheet of paper to get a sense of the pattern first…*

{% include gallery %}  
➡️ [#1 Solution](https://editor.p5js.org/jyk/sketches/L7HQXUsG-Q)  
➡️ [#2 Solution](https://editor.p5js.org/jyk/sketches/lFcZtVJf0)  
➡️ [#3 Solution](https://editor.p5js.org/jyk/sketches/bn-SKEAW7)  


## 3: Adding Variance with Random Elements
![Incorporating Random Elements]({{ "/assets/images/curriculum/Unit-7_Sample-4.png" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/hPcZzmaOj) 

If you want to add some seemingly organic variation within the loop, you can incorporate the [random()](https://p5js.org/reference/p5/random/) function. This function generates a pseudo-random number between a specified range. When using the random for a still drawing, it might be a good idea to move your code into the set-up function. This will avoid creating a flashing and chaotic animation as the random numbers would otherwise be newly generated every time the draw function loops.

In this example, we’ll generate random numbers between 0 and 255 each time the loop iterates, and apply those numbers to the colors of the circles. In order to keep the code a little bit easier to read, we’ll use variables to refer to those numbers. 

```js
function setup() {
  createCanvas(400, 400);
  
  background(255, 255, 255);
  
  noStroke();
  for (let y = 0; y <= 400; y += 20) {
    let r = random(0, 255);  // generating a random number between 0 and 255 every time the loop iterates
    
    fill(r, 100, 100); // using that number for the red value
    ellipse(100, y, 15, 15);
    
    let g = random(0, 255);
    fill(100, g, 100); 
    ellipse(200, y, 15, 15);
    
    let b = random(0, 255);
    fill(100, 100, b); 
    ellipse(300, y, 15, 15);
  }
}
```
*Note that our drawing is within the setup() function and not the draw() function. Can you guess why?*

## 4: Grids with Nested For Loops
![Putting a loop within a loop.]({{ "/assets/images/curriculum/Unit-7_Sample-5.png" | relative_url }})  
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/g0XLwASAH) 

For the purposes of a simple drawing, a lot can be achieved with layering multiple for loops. But grid like structures can be achieved with nested for loops, or loops inside of loops. 

To start off with, let’s start with a row of repeating circles. We’ll use the counter variable c for columns:
```js
for (let c = 0; c <= 400; c += 20) {
    ellipse(c, 20, 10, 10)
}
```

If we want to repeat this row in order to start a grid, we can of course repeat the loop itself:
```js
for (let c = 0; c <= 400; c += 20) { // first row of repeating circles
    ellipse(c, 20, 10, 10);
}
  
  for (let c = 0; c <= 400; c += 20) {  // second row of repeating circles
    ellipse(c, 40, 10, 10);
}
  
  for (let c = 0; c <= 400; c += 20) {  // third row of repeating circles
    ellipse(c, 60, 10, 10);
}
```

Notice that the code for the three loops above are nearly identical except for the y-position of the ellipse. By applying the same logic we used to create the first loop, we can incorporate an additional loop for the repeating rows. We’ll use the counter variable r to indicate rows. 
```js
for (let r = 0; r <= 10; r+= 20) { // this loop will only repeat once
  for (let c = 0; c <= 400; c += 20) {
      ellipse(c, r, 10, 10);
  } // end inner for loop
} // end outer for loop
```

To start with and get a closer look of the , we’ve set the outer loop that sets the r variable to repeat once. You can see that while the r loop repeats only once, the inner loop (using the c variable) repeats from start to finish, drawing all of the circles in a line from x-position 0 to 400. 

In other words, each time that the outer loop iterates, the inner loop will occur from start to finish. If we change the outer loop to run three times, you can see that the inner loop has run from start to finish three times: 
```js
for (let r = 0; r <= 40; r+= 20) { // this loop will only repeat once
  for (let c = 0; c <= 400; c += 20) {
      ellipse(c, r, 10, 10);
  } // end inner for loop
} // end outer for loop
```

Now you can create a grid, with the ability to adjust the spacing between columns and rows: 
```js
for (let r = 0; r <= 400; r+= 50) { // spacing the rows out more than the columns
  for (let c = 0; c <= 400; c += 20) {
      ellipse(c, r, 10, 10);
  } // end inner for loop
} // end outer for loop
```

This logic, along with the [random()](https://p5js.org/reference/p5/random/) function can be used to create something like a brick wall:
```js
function setup() {
  createCanvas(400, 400);
  
  background(255, 255, 255);
  
  strokeWeight(5);
  stroke(255,255,255);
  
  let brickWidth = 50;
  let brickHeight = 20;
  
  for (let y = 0; y <= height; y += brickHeight) {
    for (let x = 0; x <= width; x += brickWidth) {
      fill(128, random(0, 100), random(0, 100));
      
      if (y % (2 * brickHeight) == 0) { // Even rows: starting from x = 0
        rect(x, y, brickWidth, brickHeight);
      } else { // Odd rows: starting from x = -brickWidth/2
        rect(x - brickWidth / 2, y, brickWidth, brickHeight);
      }
    }
  }
  
}

function draw() {
}
```

You can also use this structure to create shapes like pyramids. Try uncommenting sections of the code below to see how the variables r and c are being used to generate different shapes. 

![Triangle formations with loops]({{ "/assets/images/curriculum/Unit-7_Sample-6.png" | relative_url }})

*Don’t forget to uncheck Auto-refresh just in case an error in a loop crashes the page!*
```js
function setup() {
  createCanvas(400, 400);

  background(255, 232, 241);
  
  noStroke();
  fill(54, 29, 3);
  
  /* right triangle I
  for (let r = 0; r <= 400; r+= 20) {
    for (let c = r; c <= 400; c += 20) {
      ellipse(c, r, 10, 10)
    } // end inner loop
  } // end outer loop
  */
  
  /* right triangle II
  for (let r = 0; r <= 400; r+= 20) {
    for (let c = 0; c <= r; c += 20) {
      ellipse(c, r, 10, 10)
    } // end inner loop
  } // end outer loop
  */
  
  /* equilateral triangle
  for (let r = 10; r <= 400; r += 20) {
    for (let c = 0; c <= r; c += 20) { // # of circles in a row is the same as the # row, e.g. three circles in the third row
      let center = width/2;
      let x = center - r / 2 + c; // Centered x position
      ellipse(x, r, 10, 10); // Ellipse with diameter 10
    } // end inner loop
  } // end outer loop
  */
}

function draw() {
}
```
