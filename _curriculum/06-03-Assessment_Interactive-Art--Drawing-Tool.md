# Assignment

🪜 This assignment is design for Higher Education. Please refer to Modifications for K-12 adjusted assignments.

**🔗 Template link here: [https://editor.p5js.org/chellyjin/sketches/ppfJ4V0YW](https://editor.p5js.org/chellyjin/sketches/ppfJ4V0YW)** 

- Review the template code:
    
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
      } else if (key == "s"){
        saveCanvas();
      } else {
        fill(255);
      }
    }
    
    ```
    

**In this assignment, you will create an interactive art piece that engages the participant** 

Feel free to incorporate images, shapes, colors, or text to your tool. 

Consider how:

- Interaction can invite the user to collectively participate in a work, it’s aspects of collaboration or contribution
- Interaction can subvert an idea, ask the user to do one thing yet provoke another
- Interaction can instigate something unexpected
- Interaction can reveal, unravel, generate a visual or audial aspect

## Modifications

*The following are recommendations.*

For K-8: Create a drawing tool using different shapes and colors. Refer to the template, and modify the code to use colors and shapes that speak to you. 

For 9-12: Create a drawing tool surrounding a theme of your choosing. All brushes, colors, and images contribute to one overarching idea and concept. 

## Assessments

As an educator and facilitator, we’re looking for a thorough understanding of:

- Logics within conditional statements
    - Can the student map out a flow chart of how their code will function? (Start with paper and pen, and draw out what the flow chart might look like, ie. pseudocode)
    - Can the student properly interpret the differences between an If-then, If-then-else, and Else-if?
- Mouse functions vs. Key functions
    - Can the student recognize how the Mouse interactions differ from the Key interactions? What are the affordances of using a key vs. a mouse in different instances (ie. a mouse is best used for drawing, whereas a key can be used for options). And also identify their similarities in the logic?
- Interactivity in the arts
    - Can the student integrate a form of interaction (inviting the user to click, press a key) to generate a new, richer, or unique meaning and perspective in an art piece?