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