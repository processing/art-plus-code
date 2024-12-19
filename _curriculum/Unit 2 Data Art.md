# Unit 2: Data Art

## Introduction

*How can art transform our relationship to data and information? How can we leverage computation’s ability to cull, sort, and interact with data to produce meaningful or exciting artwork? How might data and its uses engage the audience more deeply?* 

A fundamental concept in code is the input and the output — taking data in, and creating, refining, remapping something from it. Data, in this sense, is broader than the simple spreadsheet of numbers; but rather, the concept of how information is circulated throughout a system for optimization or curation. Data has become ubiquitous and far-reaching; from the ways that bits and bytes are physically stores in data farms across the U.S. to its persistence in organizing or defining humans in social media algorithms. However, we can use this concept of the structure in data to look at how modern and contemporary artists are using all kinds of data and information to create meaningful artwork to reflect, resist and understand the current condition.

In this topic, we’ll use p5.js to create a sound-reactive art project, using variables to understand the way data can feed into various inputs and output.

***Related spheres: Data Visualization, Infographic Design, Immersive Data Installations***

## References & Artworks for Discussion

Golan Levin, [Re:FACE](https://www.flong.com/archive/projects/reface-anchorage/index.html)

Refik Anadol, [Machine Hallucinations](https://refikanadol.com/works/machine-hallucinations-sphere/)

Refik Anadol, [Archive Dreaming - AI Data Sculpture](https://refikanadol.com/works/archive-dreaming/) 

Aaron Koblin, [Flight Patterns](https://www.aaronkoblin.com/project/flight-patterns/) 

Romi Morrison, [Decoding Possibilities](https://elegantcollisions.com/decoding-possibilities) 

Romi Morrison, [The Future Conditional](https://elegantcollisions.com/the-future-conditional) 

Romi Morrison, [Rituals of Black Fugitivity](https://elegantcollisions.com/rituals-of-black-fugativity-p)

## Related Artists Discussion Questions

1. In what ways do these artists challenge traditional notions of computation and coding? Conversely, how might they challenge traditional notions of art?
2. Some of the artists are utilizing art as a visualization technique for the data they’re wishing to delve deeper in; whereas some artists are utilizing art as a means to disrupt or remix the data from its initial origins to reproduce new meaning. What are some ways you’ve seen artists or communities take information and data to help bridge various understandings, reconnect to histories that were suppressed, or highlight archives that might be lost in sands of time? 
3. Romi Morrison’s work takes physical manifestations of data (archived prints, archival material, and primary sources) and revisits them in a curation that allows for deeper conversation. How does this change or illicit new understandings of data in art? 

---

## Let’s make — Sound-reactive Mask!

**🔗 Template link here:** [https://editor.p5js.org/chellyjin/sketches/D10NZG0tW](https://editor.p5js.org/chellyjin/sketches/D10NZG0tW) 

**🖼️ Example Link here:** [https://editor.p5js.org/chellyjin/sketches/NDZxQRSia](https://editor.p5js.org/chellyjin/sketches/NDZxQRSia) 

![Screenshot 2024-07-29 at 11.25.16 PM.png](Unit%202%20Data%20Art%2012f5cf001d4e811f9eb0eeb85cc89b1d/3798256c-a8c7-4514-9ec1-b73d67367c64.png)

## What we need to begin

- Computer with p5.js on web browser (Google Chrome)
- Microphone (Built in or External)

## Objectives

- Understanding the basics of variables (storing, containing or passing data), inputs, and outputs
- Becoming comfortable with creating variables, integrating arithmetic, as well as using new functions (ie. map() or constrain() ).
- Creating a sound-reactive illustration or face mask that interacts to a mic input’s volume.
- Learning about how artists use data in their practice, how variables works a metaphor for data art, and various data artists.

---

# Unplugged Activities

[Untitled](Unit%202%20Data%20Art%2012f5cf001d4e811f9eb0eeb85cc89b1d/Untitled%2012f5cf001d4e812894cbcada87c26b14.csv)

---

# The Lessons

⏰ Each of the 2 lessons will take approximately 20-25 minutes

🔗 Template link here: ****[https://editor.p5js.org/chellyjin/sketches/D10NZG0tW](https://editor.p5js.org/chellyjin/sketches/D10NZG0tW) 

## Vocabulary

1. Variables
2. Special Variables

## Lesson Plan 1: Introducing Variables

**What is a Variable?**

- A variable stores a value in memory so that it can be used later in a program.
- A variable can be used many times within a single program, and the value is easily changed while the program is running.
- The primary reason we use variables is to avoid repeating ourselves in the code.

### **How to make a Variable**

Steps 1. Declare 

- You can name them anything you’d like
- “Let” declares and initializes the variables

<aside>
🧠

Teacher Trick:

I like to think of it like “god” saying “**let** there be light!,” 

By declaring with “let”, we’re proclaiming something (a variable) into existence in our world of code. 

</aside>

Step 2. Assign a value 

- “=” assigns a value. When we say let y = 60 we’re saying now there is a y and it holds the value 60.

Step 3. Use it! 

- And then we can use it anywhere in lieu of 60!

### **Special Variables**

These are existing variables, initialized and defined by the programmers who made p5.js following some kind of convention. They make our lives a little easier and can do cool things, for example:

- mouseX, mouseY;
- use mouse to control position of ellipse
- use mouse to control scale
- use mouse to control color
- create a simple drawing program
- windowWidth, windowHeight, width, height, img.width, img.height
- Indicated by the pink color in code.

**mouseX + mouse Y**

```jsx

function setup() {

	createCanvas(600, 400);

	fill(0, 102);

	noStroke();

}

function draw() {

	background(mouseY); // background color changes based on mouseY

	ellipse(300, 200, mouseX, 50); // width changes based on mouseX

	ellipse(mouseX, mouseY, 10, 10); // ellipse follows mouse

}
```

**width and height**

```jsx
function setup() {
	createCanvas(480, 120);
}

function draw() {  
	background(204);
  line(0, 0, width, height);  // Line from (0,0) to (480, 120)
  line(width, 0, 0, height);  // Line from (480, 0) to (0, 120) ellipse(width/2, height/2, 60, 60);
}

```

### This Unit is called “Data Art” for a reason..

Even if we’re not yet utilizing large data models (like in machine learning) , spreadsheets of data (ie. sheetsDB), or open-source databases to make art — we’re still using data!~

**console.log()**

There is a cool function called console.log() in p5.js which is great to use for debugging your code. Console.log() can be used in a variety of ways, from adding it to places to check if the code you’ve written is working as you intended, or in this case, to see what is stored inside a variable!

Learning about our Special Variables, try putting them into Console.log to see what happens?

```jsx

function setup() {

	createCanvas(600, 400);

	fill(0, 102);

	noStroke();

}

function draw() {

	background(mouseY); // background color changes based on mouseY

	ellipse(300, 200, mouseX, 50); // width changes based on mouseX

	ellipse(mouseX, mouseY, 10, 10); // ellipse follows mouse
	
	console.log(mouseX, mouseY);

}
```

Below your code, is a grey box called the “Console” — after pressing Play, you should see number appear. Can you figure out what the numbers are?

- 🙋🏻‍♀️ Answer
    
    It’s the coordinates of your Mouse position! It’s telling us where our cursor is in the canvas’ space. 
    

Now, we can clearly and plainly see that mouseX and mouseY are storing and rewriting new values of data based on where you mouse position is. Data isn’t just a spreadsheet, but “the quantities, characters, or symbols on which operations are performed by a computer, being stored and transmitted in the form of electrical signals and recorded on magnetic, optical, or mechanical recording media” (Oxford Language Dictionary).

We can understand Data more expansively, and see how using variables is storing information (data) and then enabling us to utilize it in artistic, creative ways. 

## Lesson Plan 2: What you can do with Variables

**Prompt**: Why might creating a variable be helpful, valuable or efficient?

### Repeatability

I want to make 3 ellipses

```jsx
function setup() {

	createCanvas(600, 600);

}

function draw() {

	ellipse(75, 60, 80, 80);   // left

	ellipse(175, 60, 80, 80);  // middle

	ellipse(275, 60, 80, 80);  // right

}
```

But do you see all those redundant numbers?

Instead of having to repeat the same number over and over again, I can store numbers that will always continue to be the same value as one variable:  

```jsx
let y = 60; // 100

let d = 80; // 130

function setup() {

	createCanvas(600, 600);

}

function draw() {

	ellipse(75, y, d, d);   // left

	ellipse(175, y, d, d);  // middle

	ellipse(275, y, d, d);  // right

}
```

In the example above, I’ve made:

- let y = 60;  a variable called “y” to represent the y coordinate value I want all my circles to be in (so they’re on a straight line!) at 60px from the top
- let d = 80; is a variable representing my diameter — how big I want the circles to be. Because I want all my circles the same size.

Now, remember, we can name these WHATEVER we’d like: apple, oranges, we can even call is X but use it for the values of Y! 

BUT, it’s really in the best interest for your future self, as well as good coding hygiene for future sharing with other coders, to name your variables, functions or arrays as self-descriptive names. You can certainly name however you’d like but making it easier for yourself to debug later is always a good practice.

Also, using variables makes it super easy to make changes for later. 

Instead of having to rewrite all new values, I can simply change the value at the top and the change will trickle throughout: 

```jsx
let y = 60; // 100 or change it to whatever value or size you want! 

let d = 80; // 130 or change it to whatever value or size you want! 

function setup() {

	createCanvas(600, 600);

}

function draw() {

	ellipse(75, y, d, d);   // left

	ellipse(175, y, d, d);  // middle

	ellipse(275, y, d, d);  // right

}
```

### Arithmetic

**Add arithmetic to your variables!**

- variable arithmetic (you can modify variables)
- order of operations (), * /, + -
- +=, ++, –
- You can use this to make increments of your variables, animate your elements, and so much more!

Let’s revisit our 3 circles: 

```jsx
let y = 60; // 100

let d = 80; // 130

function setup() {

	createCanvas(600, 600);

}

function draw() {

	ellipse(75, y, d, d);   // left

	ellipse(175, y, d, d);  // middle

	ellipse(275, y, d, d);  // right

}
```

If you notice, each of the circle’s X value is following some kind of an increment. It’s adding 100px every time!

We can utilize the power of variables WITH arithmetic to make it easier for us. 

```jsx
let x = 75; // where we want the first circle's X to start

let y = 60; // 100

let d = 80; // 130

function setup() {

	createCanvas(600, 600);

}

function draw() {

	ellipse(x, y, d, d);   // left

	ellipse(x+100, y, d, d);  // middle

	ellipse(x+200, y, d, d);  // right

}
```

OR we can even modify it further. How would you go about it?

- Answer
    
    There are SO many ways you can answer this question actually, and there is no right or wrong way. Here is one example of how I might streamline this so I can make iterations or easy changes in the future:
    
    ```jsx
    let x = 75; // where we want the first circle's X to start
    
    let y = 60; // 100
    
    let d = 80; // 130
    
    let s = 20; // the spacing between each circle
    
    function setup() {
    
    	createCanvas(600, 600);
    
    }
    
    function draw() {
    
    	ellipse(x, y, d, d);   // x = 75, which is the same
    
    	ellipse(x + (d+s), y, d, d);  // now, we're adding the d (our circle's diameter, so they don't overlap)
    																// +s, which adds 20px gap so the circle's aren't touching
    
    	ellipse(x + (2*(d+s)), y, d, d);  // and then multipled by 2 so it keeps the same distance + width 
    
    	ellipse(x + (3*(d+s)), y, d, d); // and then we make it super easy for our future selves
    	
    	ellipse(x + (4*(d+s)), y, d, d);
    }
    ```
    

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

- replacing the value
    - updating itself with new information - ie. x = x+1;
    - if using “let” changing what the variable is used for: holding numbers or text or array of values
- one way we can check what is stored inside the variable is to use : “console.log” — how to see the output of variables: vol
    - using it to see all the “data” and numbers taken from the microphone

---

# Assignment

🪜 This assignment is designed for Middle school and older. Please refer to Modifications for K-12 adjusted assignments.

**🔗 Template link here:** [https://editor.p5js.org/chellyjin/sketches/D10NZG0tW](https://editor.p5js.org/chellyjin/sketches/D10NZG0tW) 

- Review the template code:
    
    ```jsx
    // This template was modified from a template created by Lauren Lee McCarthy: https://lauren-mccarthy.com/
    // click on the canvas to enable the mic
    
    let mic;
    let vol = 0;
    
    function setup() {
      createCanvas(600, 600);
      rectMode(CENTER);
    }
    
    function draw() {
      if (mic) updateVol();
      
      // START DRAWING HERE
      background(200);
      
      let d = map(vol, 0, 1, 100, 600);
      
      console.log(vol);
      // strokeWeight(1);
      ellipse(400, height/2, d, d);
      ellipse(200, height/2, d, d);
      
      let sw = map(vol, 0, 1, 1, 200);
      strokeWeight(sw);
      rect(300, 400, sw*30, 50);
      
      let c = map(vol, 0, 0.3, 0, 255);
      fill(c);
      
      
      
    }
    
    function mousePressed() { // setup audio
      mic = new p5.AudioIn();
      mic.start();
      userStartAudio();
    }
    
    function updateVol() {
      // get the overall volume (between 0 and 1)
      let v = mic.getLevel();
      // "smooth" the volume variable with an easing function
      vol += (v-vol)/3;
      
    }
    ```
    

**In this assignment, you will create an sound-reactive art piece.**

This can be a sound-reactive mask someone might wear (ie. put the sketch on your phone, and hold the phone in front of your face) or a character who moves to a spoken word piece, or utilizing the volume variable to modulate unique visuals. 

Consider how:

- Sound is featured in your work. How might you pair the words or sounds you’ll say with the visuals you see and interact with?
- Volume can be used to create a unique visual and audial experience.
- Masks are used in various cultures, traditions and representations. How have other artists used masks to explore identity and history?

## Modifications

*The following are recommendations.*

For K-8: Create a sound-reactive face. Use to the template, and allow students to modify the code’s colors using fill(). 

## Assessments

As an educator and facilitator, we’re looking for a thorough understanding of:

- Logics of Input and Output
    - Can the student explain how to set up a variable; and what is being “stored” inside the variable?
    - Can the student properly interpret the differences between an variables they make and special variables from p5.js?
- Console Log and Debugging
    - Can the student be self-motivated to try and debug their code using variables inside the console.log() function?
- Data in the arts
    - Can the student expand their interpretation of “data” and “data art” (the information we gather and curate) to generate a new, richer, or unique meaning and perspective in an art piece?