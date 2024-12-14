---
# This is the frontmatter
title: "Digital Drawing Tool: Practice Exercises" # Title and Heading 1
permalink: /1-practice/ # Give your page a permalink
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

### Mouse Interactions

**Start here (Easy)**

How might you make your mouse stamp a circle on Mouse Pressed and draw a square on Mouse Dragged? 

- 🙋*Answer*
    
    ```jsx
    
    function setup() {
      createCanvas(400, 400);
    }
    
    function draw() {
    }
    
    function mousePressed(){
      ellipse(mouseX,mouseY, 50);
    }
    
    function mouseDragged() {
      rectMode(CENTER);
      rect(mouseX,mouseY, 50, 50);  
    }
    ```
    

**Level up (Medium)**

How can you make a circle appear in the center of the page when mouse is pressed and disappear when mouse is NOT pressed? 

- 🙋*Answer*
    
    Here is an example using an if-then-else statement using the mouseIsPressed boolean. 
    
    ```jsx
    function setup() {
      createCanvas(400, 400);
    }
    
    function draw() {
      if (mouseIsPressed) {
        circle(width/2, height/2, 100);
      } else {
        background(255);
      }
    }
    ```
    
    But, there are many ways we could achieve this as well, here’s another example using: functions mousePressed() and mouseReleased()
    
    ```jsx
    function setup() {
      createCanvas(400, 400);
        background(255);
    }
    
    function draw() {
    
    }
    
    function mousePressed(){
      circle(width/2, height/2, 100);
    }
    
    function mouseReleased(){
      background(255);
    }
    ```
    

**Extra push (Hard)**

Can you make a “button”? This Button will change the color of a circle depending on the different mouse events we can use. Consider what does the “button” (ie. a circle or square) look like on press, vs. on release vs. dragged. 

- 🙋*Answer*
    
    You can interpret this question any way you like, and the main idea is that you consider different states of the button based on different interactions. There are no right or wrong answers, as long as you establish some kind of pattern to your interaction. Feel free to reference button states in UX Design for inspiration. The following is one simple example, but please expand on this as you desire! 
    
    ```jsx
    let circleW = 100; // establishes circle's width -- easier to change in future
    let d; // we will use this variable "d" for distance
    let selected = false; // we will create our own boolean variable set as false
    
    function setup() {
      createCanvas(400, 400);
      textAlign(CENTER);
    }
    
    function draw() {
      // start with a background color as white
      background(255);
      
      // start with a white circle as default
        fill(255);
        circle(width / 2, height / 2, circleW);
      
      // assign variable "d" a value
      // dist is a function to calcuate the distance between 2 points
      // this is the syntax: dist(x1, y1, x2, y2)
      // so we're calculating the distance of where your mouse is (x1,y1) to the center of the circle (x2,y2)
      d = dist(mouseX, mouseY, width / 2, height / 2);
    
      if (mouseIsPressed && d < circleW / 2) {
        // if the mouse is pressed and the mouse is in the area of the circle...
        //... pick up a solid green marker, draw a circle, add text and set our boolean "selected" as true
        fill(0, 255, 0);
        circle(width / 2, height / 2, circleW);
        text("select", width/2, height/2 + 100);
        selected = true;
        
      } else if (d < circleW / 2) {
        // else if: the mouse is just in the area of the circle
        // think of it as: if mouse hovers over the circle's area...
        // .. pick up a light green marker, and draw a new circle
        fill(0, 255, 0, 50);
        circle(width / 2, height / 2, circleW);
        text("hover", width/2, height/2 + 100);
        
      } else {
        // .. otherwise, pick up a white marker and draw a new circle
        fill(255);
        circle(width / 2, height / 2, circleW);
      }
      
      // if selected is true (after being clicked in the area), then add some black text
      if (selected == true){
        fill(0);
        text("selected", width/2, height/2 + 200);
      }
    }
    ```
    
### If/Else Statements

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
    
### Key Interactions

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
    

**Level up (Medium)**

How could I re-write the drawing tool code to use keyIsPressed? 

- 🙋 *Answer*
    
    Simply, we can move what was once in Key Pressed inside keyIsPressed in the draw() function. We can even clean it up further by making it a large, if-then-else statement too. 
    
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
        } else if (key == "r") {
          fill(255, 0, 0);
        } else if (key == "g") {
          fill(0, 255, 0);
        } else if (key == "b") {
          fill(0, 0, 255);
        } else if (key == "x") {
          fill(random(255), random(255), random(255));
        } else if (key == 0) {
          background(0);
        } else {
          fill(255);
        }
      }
    }
    
    ```
    

**Extra push (Hard)**

How can I save the canvas as an image with a specific key press? (look into the references for a save function). 

- 🙋 *Answer*
    
    Look into the p5.js saveCanvas() function, reference link here: [https://p5js.org/reference/p5/saveCanvas/](https://p5js.org/reference/p5/saveCanvas/) 
    
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
      text("Press s to save.", 10, 125);
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
        background(0);
      } else if (key == "s"){ // if we press "s"
        saveCanvas(); // we'll save the canvas to your computer 
      } else {
        fill(255);
      }
    }
    
    ```
