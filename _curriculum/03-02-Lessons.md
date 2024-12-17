---
# This is the frontmatter
title: "Art & Time: Introduction & Inspiration" # Title and Heading 1
permalink: /artTime-introduction/ # Give your page a permalink
published: true

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

# Art & Time

> I believe that if one takes a closer look at things, there is always a sort of sense of time involved. And I am very interested in how to make that visible. And this time that you take for looking at things, it also becomes a matter of space, of seeing space.
>
> \- Olafur Eliasson, 2014 lecture at the Massachusetts Institute of Technology

How do artists engage with the concept of time? This can include time-based media (a term describing art that unfolds over a span of time such as performance art, video, animation), illustrations of motion, or 2D drawings made over an accumulated time period. In this unit, we’ll use some of the P5JS tools that work with the computer’s clock and conditional statements to incorporate the element of time through animation into our digital drawings. 

The goal of this sequence is to have students create an original design for a clock, or find an interesting way of representing the passage of time. As some age groups and cohorts can find working with abstraction challenging, the visual ideas in this topic can be differentiated for the student group in two ways, pursuing abstraction and/or using text as a graphic element. Coding examples as well as artistic precedents for both directions are provided.

{% include gallery caption="Design an artwork that functions as a clock in P5JS!" %}

## Objectives
- Creating individual interpretations of "universal concepts"
- Working with automated elements in a composition
- **Visual Arts Vocabulary**: text, abstraction, movement


## Technical Terms & P5JS Elements
- [text()](https://p5js.org/reference/p5/text/) and text formatting functions
- escape sequences \n, \’, \”
- clock methods [hour()](https://p5js.org/reference/p5/hour/), [minute()](https://p5js.org/reference/p5/minute/), [second()](https://p5js.org/reference/p5/second/)
- arithmetic operators and expressions + - * /
- conditional statements if/else
- boolean expressions and operators >, <, >=, <=, ===, !==, &&, ||
- modulo operator %


  
## References & Artworks for Discussion: Line Quality
* Ho Tzu Nyen, [T for Time](https://www.singaporeartmuseum.sg/Art-Events/Exhibitions/Ho-Tzu-Nyen-Time-and-the-Tiger#artworks), 2023 - 
* Nam June Paik, [TV Clock](https://americanart.si.edu/artwork/tv-clock-80132), 1963/1981, Smithsonian American Art Museum
* Spencer Finch, [A Certain Slant of Light](https://www.spencerfinch.com/a-certain-slant-of-light), 2014, Morgan Library
* Yuko Mohri, [3 Musics](https://mohrizm.net/works/3-musics/), 2021
* Carlo Carrà, [Parole in Liberta](https://www.researchgate.net/figure/Parole-in-Liberta-Carlo-Carra-1914-Meggs-Purvis-2006-p-252_fig12_216473323), 1914
* Archie Moore, [kith and kin](https://www.kithandkin.me/documentation/panoramic), 2024, Venice Biennale Australia Pavilion
* Hiroshi Sugimoto, [Theatres](https://www.sugimotohiroshi.com/new-page-7), 1976 - 
* On Kawara, [Date Paintings](https://www.davidzwirner.com/artists/on-kawara), 1966 - 2013
* Christian Marclay, [The Clock](https://www.tate.org.uk/art/lists/five-ways-christian-marclays-clock-does-more-just-tell-time), 2010, Tate Modern


## Timeline
This project will take approximately four 45minute sessions:
1. Discussing artists, warm up activities, drafting a design, P5JS review
2. Working with text and clock variables
3. if/else statements, executing the clock design
4. Finalizing the clock design, sharing out


### Warm-Up Exercises
Some options for unplugged exercises:
- Mindfulness
  - The goal of this activity is to share a meditative activity with students and also practice a little bit of mindfulness. Select at least 2 amounts of time including one ‘short’ and one ‘long’ such as 30 seconds and 10 minutes. Sit with students in silence for that duration of time, then discuss the physical experience of that time. 
  - Some ways of facilitating that discussion include pair-sharing (small groups of students share with each other their experiences of that time and each group shares out a summary) and creating a word cloud of the board of key words students would use to describe their experience (“long”, “short”, “surprising”)
  - The goal of the exercise is for the students to have some concrete descriptors to draw from and reference as they create their designs. Helpful questions for students to discuss might be “What kind of physical sensations did you feel in your body, such as twitchiness or calm”, “What did you focus your eyesight on during this unit of time?”, “What are some things you noticed in the room that you might not have noticed before?” and “What emotions might you connect with these units of time?”

- Times of Day
  - Have students write or sketch an object or location at different times of day, from morning, mid-afternoon, to evening such as a plant or room. 
  - Consider the intensity and color of light, surrounding objects, any possible movements.

- Long exposure photography
  - If a dark environment and photographic equipment (cameras, tripods) are available, students can try out long exposure photography to gain a sensitivity for light-based information accumulating on a surface.
  - In pairs or groups of three, students set up cameras (or smart devices with manual camera apps installed) with tripods. The cameras should have long shutter speeds, ranging from 1 second to manually open to create long exposure photographs. 
  - Incorporating lights, either with small LEDs or the flash of their phone can allow for students to create light paintings.

- Drafting an Original Clock Design
  - To prepare for the project  of designing a clock, students draft a design for an original clock. Depending on the age group and differentiation needs of the students, useful guidelines or constraints might be “no numbers”, “only use the shapes we’ve tried so far in P5JS”
  - Have students create a design for a clock using paper cutouts of shapes (á la Matisse) or letters (in the style of Italian Parole in Liberta). 

---
# This is the frontmatter
title: "Art & Time: Lesson Plans" # Title and Heading 1
permalink: /artTime-lessons/ # Give your page a permalink
published: true

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
# Art & Time

## Lesson Plans & Technical Steps

### Step 1: Working with Text
[Sample Sketch](https://editor.p5js.org/jyk/sketches/l6NvshaaP)

In the last topic, we worked with different shapes such as rectangles and ellipses to create drawings. In P5JS, we can also incorporate text into our drawings. To display text, use the text() command: 
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

You can also customize the way the text looks using these methods:
```js
textFont("font name in between quotes");
textAlign(CENTER); // Where you want the x, y position values to refer to. Also LEFT, RIGHT
textAlign(CENTER, TOP); // Adding a second value to this command will add vertical alignment. Also BOTTOM, BASELINE, CENTER
textSize(#); // how many pixels tall do you want your text to be
textStyle(BOLD); // also ITALIC, BOLDITALIC, NORMAL
textWidth(#); // how much horizontal space you want the text to take up
textWrap(WORD); // if you want the automatic line breaks to happen at words 
```

Just like the fill() and stroke() commands, it’s good practice to have these lines before the text() command they are related to. 
	
When using the textFont() command, the font needs to be installed on your computer. You can download and install Opensource fonts from Google Fonts. 

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
[Sample Sketch](https://editor.p5js.org/jyk/sketches/ToNnvOTSi)

In the last topic, we worked with data that the P5JS library allows us to access easily like mouseX and windowWidth. Here, we’ll work with some more tools that allow us to work with time. These commands work with the clock on your computer:
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
[Sample Sketch](https://editor.p5js.org/jyk/sketches/bW8K_lRzg)

We can use these clock values along with some arithmetic operators (+ - * /) to create a drawing that moves according to the time of day and design our own clock. This sketch incorporates arithmetic expressions like (hour() * 22) so that we can adjust the values to fit the dimensions of our drawing.
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
[Sample Sketch](https://editor.p5js.org/jyk/sketches/V5XyoyD41)

To gain more functionality from the clock variables, we can use if/else statements, also referred to as conditional statements. The syntax for an if/else statement looks like this: 
```js
if (boolean expression) {
  // code to be executed
} else {
  // code to be executed
}
```

If the boolean expression between the parentheses after the keyword if evaluates to true, then all the code between the curly brackets will execute. Otherwise, the code between the curly brackets following the keyword else will execute. 

Booleans expressions are essentially statements that evaluate to true or false. Like we use arithmetic operators (+ - * / %) for arithmetic expressions (x + 10), we use boolean operators (=== > >= < <= !==) for boolean expressions. Here are some examples:
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

We can also use and && and || operators to create ranges of options for our if/else statements.
```js
if (mouseX < 100) { // checking if value of mouseX is less than 100 (non-inclusive)
  fill(255, 255, 255);
} else if (mouseX >= 100 && mouseX < 200) { // checking if value of mouseX is greater than 100 (inclusive of 100) and less than 200
  fill(255, 0, 0);
} else if (mouseX >= 200 && mouseX < 300 {
  fill(0, 255, 0);
} else { // for any possibility not checked for already
  fill(0, 0, 255);
}

rect(100, 100, 40, 40);
```

We can use boolean expressions and if/else statements to display different drawings depending on the time of day. The order of if statements is important, as it sets 
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

We can also create a flashing effect using the modulo operator %. The mod operator is an arithmetic operator similar to /. If using the / gives us the quotient of a division, % will give us the remainder: 
console.log(13/2); // will print 6.5, the quotient
console.log(13 % 2); // will print 1 because the remainder of 13/2 is 1


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

---
# This is the frontmatter
title: "Art & Time: Assessment Activities" # Title and Heading 1
permalink: /artTime-assessment/ # Give your page a permalink
published: true

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

# Art & Time

## Assessment Activities

Once ready, students should use the tools at hand, drawing, if/else statements, arithmetic and boolean operators to create their original clock design. 

Once the sketches are complete, they can be shared using a link to the editor. The links can be compiled into a shared document or spreadsheet. 

Students can share their work with their peers with a gallery walk:
- Students open up their sketch in full screen mode at their stations or on their desk. Students can provide a description of their approach next to their computer, similar to exhibition wall text.
- The class moves around the room to look at their peer’s work. 
- Students can leave each other feedback using post-it notes. 

Students can also share their tools and resulting drawings. Questions to consider for discussion and reflection:
- What were some of the specific sensations and feelings you wanted to convey with your clock? What visual elements did you use to convey those sensations and feelings?
- How did you incorporate the dynamic variables such as hour, minute, and second values into your sketch? Why did you choose those elements for those values?
- Were there moments of ‘unlearning’ you came across? (e.g. sticking too closely to a sundial design)



## Checking for Understanding

Do students grasp the core concepts of the topic?
Are the students applying text, drawing, clock components of P5JS to support the goals of their design? 
Are students trying new ways of conveying information?
Is the code written by the student free of errors that prevent the code from working?

Are the students comfortable with the technical aspects of the topic?
- Are students combining elements like if/else statements and boolean operators to create multiple possibilities for their design? 
- Are students applying computational logic effectively in their work (e.g. being deliberate about the order of their if/else statements)?
- Is the code free of errors and executing in the way the student intended?

Are the students using their creative and visual communication skills?
- How are students engaging with representing concepts through abstraction? 
- How responsive are students to feedback about their designs?
- Are students making an effort to deviate from familiar methods of representing time?

How are the students keeping track of their personal and artistic growth?
- How are students articulating their goals and process throughout the design and building stages?
- How are students providing feedback to each other? Is the feedback constructive and specific?

