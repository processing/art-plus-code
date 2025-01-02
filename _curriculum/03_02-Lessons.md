---
# This is the frontmatter
title: "Art & Time" # Title and Heading 1
permalink: /artTime-lessons/ # Give your page a permalink
published: true

---
## Lesson Plans & Technical Steps

### Step 1: Working with Text
![Incorporating text into a P5JS sketch.]({{ "/assets/images/curriculum/Unit-3_Sample-2.gif" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/l6NvshaaP)

You'll probably be familiar with using different shapes such as [rectangles](https://p5js.org/reference/p5/rect/) and [ellipses](https://p5js.org/reference/p5/ellipse/) to create drawings. In P5JS, we can also incorporate text into our drawings. To display text, use the [text()](https://p5js.org/reference/p5/text/) command: 
```js
text("your text here", x position, y position);
```
 
Notice that the text goes between two quotation marks. You can use double or single quotations as long as they are paired up. For displaying special characters such as quotation marks or line breaks, you can indicate that using a backslash. These are called escape sequences.
```js
text("your text \n here", x position, y position); 
// will display 
// your text
// here
text("your \'text\' here", x position, y position); // will display your 'text' here
```

You can also customize the way the text looks using these [methods related to typography](https://p5js.org/reference/#Typography):
```js
textFont("font name in between quotes");
textAlign(CENTER); // Where you want the x, y position values to refer to. Also LEFT, RIGHT
textAlign(CENTER, TOP); // Adding a second value to this command will add vertical alignment. Also BOTTOM, BASELINE, CENTER
textSize(#); // how many pixels tall do you want your text to be
textStyle(BOLD); // also ITALIC, BOLDITALIC, NORMAL
textWidth(#); // how much horizontal space you want the text to take up
textWrap(WORD); // if you want the automatic line breaks to happen at words 
```

Just like the [fill()](https://p5js.org/reference/p5/fill/) and [stroke()](https://p5js.org/reference/p5/stroke/) commands, it’s good practice to have these lines before the text() command they are related to. 
	
When using the [textFont()](https://p5js.org/reference/p5/textFont/) command, the font needs to be installed on your computer. You can download and install Opensource fonts from [Google Fonts](https://fonts.google.com/). 

You can also specify alternative fonts, in case there is an issue with displaying the font specified. Typically, the order of listing fonts goes from specific to general:
textFont("Helvetica Neue", "Arial", "sans-serif");


Here, the intended font is Helvetica Neue which is not necessarily installed on every single computer. If Helvetica Neue is unavailable, Arial will display. In the unlikely but possible likelihood Arial is not installed, the computer’s default sans-serif font will display.

 In this example, a simple message displays some text on our canvas. 
```js
function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(0,0,255);
  fill(255,255,255);

  // customizing our text
  textFont('Helvetica Neue', "Arial", "sans-serif");
  textAlign(CENTER);
  textSize(40);
  // displaying text
  text("I'm glad you're here.", 300, 220);
}
```



### Step 2: Clock Variables
![Displaying the hour, minute, and second.]({{ "/assets/images/curriculum/Unit-3_Sample-3.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/ToNnvOTSi)

The P5JS library includes variables that allows us to access interactive data easily like [mouseX](https://p5js.org/reference/p5/mouseX/) and [windowWidth](https://p5js.org/reference/p5/windowWidth/). Here, we’ll work with some commands that use the clock on your computer. These are:
* [hour()](https://p5js.org/reference/p5/hour/), which will return the hour on your computer's clock
* [minute()](https://p5js.org/reference/p5/minute/), which returns the current minute
* [second()](https://p5js.org/reference/p5/second/), which returns the second

These functions return the time on the local device's computer. That is, the time on the computer that is displaying the sketch. If you send the sketch to a friend in a different timezone, it will display the values from *their* clock!
```js
function setup() {
  createCanvas(600, 400);
}

function draw() {
  background(0,0,255);
  fill(255,255,255);
  
  console.log("hour is: " + hour()); // prints out the value of hour()
  console.log("minute is: " + minute()); // prints out the value of hour()
  console.log("second is: " + second()); // prints out the value of hour()

  // customizing our text
  textFont('Times New Roman');
  textAlign(CENTER);
  textStyle(BOLDITALIC);
  textSize(80);
  // displaying text
  text(hour() + ":"  + hour() + ":"  + hour(), 300, 220);
}
```

You’ll notice that we are joining text and numbers together inside the text() command with a + sign. This is called ‘string concatenation’. 


### Step 3: Designing a Clock
![Create a drawing that changes according to time of day!]({{ "/assets/images/curriculum/Unit-3_Sample-4.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/bW8K_lRzg)

We can use these clock values along with some **arithmetic operators** (+ - * /) to create a drawing that moves according to the time of day and design our own clock. This sketch incorporates *arithmetic expressions* like (hour() * 22) so that we can adjust the values to fit the dimensions of our drawing.
```js
/*
This image is inspired by the prints of Swiss artist Sophie Taueber-Arp.
*/

function setup() {
  createCanvas(480, 640);
}


function draw() {
  background(252, 250, 242);

  noStroke();
  
  fill(18, 72, 99);
  triangle(80, hour() * 22, 300, hour() * 22, 80, 640)
  
  fill(255,0,0);
  triangle(minute() * 8, hour() * 22, second() * 8, 0, 350, hour() * 22);

  fill(255,0,0);
  ellipse(100, hour() * 22, 60, 60);
  
  fill(255, 221, 0);
  ellipse(minute() * 8, 100, 60, 60);
  
  fill(57, 163, 0);
  ellipse(second() * 8, second() * 10, 60, 60);
  
  stroke(0,0,0);
  strokeWeight(4);
  line(0, hour() * 22 + 50, 480, second() * 10);
  line(80, second() * 10, 400, windowHeight - second() * 20);
  line(minute() * 4, 0, windowWidth - (minute() * 8), 720)
}
```


### Step 4: Adding Complexity with Conditional Statements
![Create a drawing that changes according to time of day!]({{ "/assets/images/curriculum/Unit-3_Sample-5.png" | relative_url }})
[➡️ Sample Sketch](https://editor.p5js.org/jyk/sketches/V5XyoyD41)

To gain more functionality from the clock variables, we can use **if/else statements**, also referred to as *conditional statements*. The syntax for an if/else statement looks like this: 
```js
if (boolean expression) {
  // code to be executed
} else {
  // code to be executed
}
```

If the boolean expression between the parentheses after the keyword **if** evaluates to *true*, then all the code between the curly brackets will execute. Otherwise, the code between the curly brackets following the keyword **else** will execute. 

*Booleans expressions* are essentially statements that evaluate to *true* or *false*. Like we use arithmetic operators (+ - * / %) for arithmetic expressions (x + 10), we use **boolean operators** (=== > >= < <= !==) for boolean expressions. Here are some examples:
```js
let age = 30;
console.log(age === 29); // === checks for equivalency, this will print out "FALSE"
console.log(age > 30); // we can use greater than or less than symbols, this will print "FALSE"
console.log(age >= 30); // this will print TRUE because we are using the greater than or equal to operator
console.log(age !== 29); // ! translates to 'not', here we are checking if age is NOT equal to 29
if (age > 30) {
  console.log("good morning");
} else {
  console.log("good evening");
}
```

We can also use AND **&&** and OR **||** operators to create ranges of options for our if/else statements.
```js
if (mouseX < 100) { // checking if value of mouseX is less than 100 (non-inclusive)
  fill(255, 255, 255);
} else if (mouseX >= 100 && mouseX < 200) { // checking if value of mouseX is greater than 100 (inclusive of 100) AND less than 200
  fill(255, 0, 0);
} else if (mouseX >= 200 && mouseX < 300 {
  fill(0, 255, 0);
} else { // for any possibility not checked for already
  fill(0, 0, 255);
}

rect(100, 100, 40, 40);
```

We can use boolean expressions and if/else statements to display different drawings depending on the time of day. The order of if statements is important, as it sets a priority order: 
```js
function setup() {
  createCanvas(600, 600);
}

function draw() {
  background(0,0,0);

  // customizing our text
  textFont("Anonymous Pro", "Courier", "monospace"); // you can use a category of font to use system defaults
  textAlign(LEFT, CENTER);
  textStyle(NORMAL);
  textSize(24);
  // displaying text

  fill(255, 255, 255);
  
  if (hour() === 10 || hour() === 15) { // if it's 10am OR 3pm, this text will display
    text("Coffee break?", 80, minute() * 10);
  } else if (hour() > 12) {
    text("Almost time to go home...", 80, minute() * 10);
  } else {
    text("Just getting started!!!", 80, minute() * 10);
  }
}
```

We can also create a flashing effect using the *modulo* operator **%**. The mod operator is an arithmetic operator similar to **/**. If using the **/** gives us the quotient of a division, **%** will give us the remainder: 
```js
console.log(13/2); // will print 6.5, the quotient
console.log(13 % 2); // will print 1 because the remainder of 13/2 is 1
```

The most common use of modulo % is to obtain an alternating pattern. For instance, every other ______. To incorporate the modulo % into a boolean statement, use this syntax: 
```js
console.log(13 % 2 === 0); // will print out FALSE

if (mouseX % 2 === 0) {
  rect(mouseX, mouseY, 20, 10);
else {
  rect(mouseX, mouseY, 10, 20);
}
```

Here, we’ll use the modulo in combination with the second() function to create a flashing effect:
```js
function setup() {
  createCanvas(600, 600);
}

console.log(13/2);

function draw() {
  background(0,0,0);

  // customizing our text
  textFont("Anonymous Pro", "Courier", "monospace"); // you can use a category of font to use system defaults
  textAlign(LEFT, CENTER);
  textStyle(NORMAL);
  textSize(24);
  // displaying text
  
  if (second() % 2 === 0) {
    fill(60, 60, 60);
  } else {
    fill(140, 255, 167);
  }
  if (hour() > 12) {
    text("Almost time to go home...", 80, minute() * 10);
  } else {
    text("Just getting started!!!", 80, minute() * 10);
  }
}
```