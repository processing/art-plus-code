---
# This is the frontmatter
title: "Generative Patterns + Weaving" # Title and Heading 1
permalink: /generativeweaving-assessment/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/thumbnails/unit8.png
    image_path: /assets/images/thumbnails/unit8.png
    alt: "Screenshot of an generative weaving pattern tool using the p5.js web editor"
    title: "Generative Weaving Pattern"

---

# Assessment Activities & Checking for Understanding

🪜 This assignment is design for Higher Education. Please refer to Modifications for K-12 adjusted assignments.

**🔗 Template link here:** [https://editor.p5js.org/chellyjin/sketches/3-7xyzKng](https://editor.p5js.org/chellyjin/sketches/3-7xyzKng) 


Review the template code:
    
    ```jsx
    
    let size = 10;

    function setup() {
      createCanvas(1080,1920);
      frameRate(1);
      noLoop();
      // noStroke();
    }

    function draw() {
      // background(255);
      rectMode(CENTER);

      // random color picker 
      let startColorR = random(50,200);
      let startColorB= random(50,200);
      let startColorG = random(50,200);

      // MOUSE REACTIVE!!! 
      // let startColorR = mouseX;
      // let startColorB= mouseY;
      // let startColorG = random(50,200);

      for(x=size/2; x<width; x += size){
        for(y=size/2; y<height; y += size){

          // COLOR 
          //for each element: add on top a different random value, so it gives a color near the starting color 
          fill(startColorR+random(100), startColorB+random(100), startColorG+random(100));
          stroke(startColorR+random(100), startColorB+random(100), startColorG+random(100));


          // DIFFERENT ELEMENTS <if-then statement>

          let selection = int(random(0,6));

          if (selection == 0 || selection == 1){
          // CIRCLE
          // draw our circles at each point, using a different size between 0 - circSize variable 
            noStroke();
          ellipse(x, y, int(random(5,size))); 
          }

          if (selection == 2){
          // RECTANGLES / SQUARE
            noStroke();
          rect(x, y, int(random(3,size)));
          }

          if(selection ==3){
            // blank space :) 
          }

          if (selection == 4){
            // LINE
            line(x - size/4,y - size/4,x + size/4, y + size/4);
          }

          if (selection == 5){
            line(x - size/4 ,y+size/4, x+size/3,y -size/4);
          }
          if (selection == 4){
            line(x - size/4,y - size/4,x + size/4, y + size/4);
            line(x - size/4 ,y+size/4, x+size/3,y -size/4);
          }
        }
      }
    }

    function keyPressed(){
      if (key == "s"){
        saveCanvas();
      }
    }
    
    ```

**In this assignment, you will create a generative weaving pattern.**

Feel free to incorporate images, shapes, colors, or text to your tool. 

Consider how:

- Loops can play with a sense of grid structure or changes over iteration
- Patterns play with a sum that is greater than the parts; pieces that constitute a unique whole
- Randomness adds a level of computational choice-making within a system of your own design
- Materializing these patterns (printing them out, using as an embroidery, crochet or beading pattern)

## Modifications

*The following are recommendations.*

For K-8: Modify the existing code template to swap out colors and shapes to create new forms. Print these patterns out and find ways to add materiality to it (sewing, gluing beads, tiles, wrapping paper).

For 9-12: Modify the existing code template or create your own generative weaving sketch. Consider adding new elements such as importing images or letter / text-based characters. Consider how you might export these pattern and use it for something new. Consider how allowing computation to randomly select pieces create for unique pattern making.  

## Checking for Understanding

As an educator and facilitator, we’re looking for a thorough understanding of:

- Logics of Loops
    - Can the student interpret a for-loop statement's outcome (using pen and paper or verbal explanation)? What does each segment of the for-loop represent? How many times will the code loop?
    - Can the student acknowledge where the code that needs to be looped goes, and what happens to it over time?
- Randomness
    - Can the student incorporate computational randomness as a source of generative inspiration? Does the student understand how to utilize the random() function and identify when they’d want to use it versus when it doesn’t fit their needs?
- Generative arts
    - Can the student engage with generative artists? Can the student create their own conclusions to methodologies of art creation with non-human entities?


