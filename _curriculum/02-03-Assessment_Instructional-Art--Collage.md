# Assignment

🪜 This assignment is design for All Levels. 

**🔗 Template link here:** [https://editor.p5js.org/chellyjin/sketches/8-TuqGyaq](https://editor.p5js.org/chellyjin/sketches/8-TuqGyaq)

- Review the template code:
    
    ```jsx
    let libraryScene;
    let book1;
    
    function preload() {
      // Upload images directly to the editor
      libraryScene = loadImage("library.jpg");
    
      // Upload images using the Image Link Address
      book1 = loadImage(
        "https://m.media-amazon.com/images/I/71FxgtFKcQL._AC_UF1000,1000_QL80_.jpg"
      );
      book2 = loadImage(
        "https://m.media-amazon.com/images/I/81q9Cy8AsDL._AC_UF1000,1000_QL80_.jpg"
      );
    }
    
    function setup() {
      createCanvas(1000, 800);
    }
    
    function draw() {
      background(libraryScene);
    
      // ADD SHAPES + COLORS
      noStroke();
      fill(201, 127, 56);
      circle(150, 150, 250);
      fill(201, 189, 56);
      rect(500, 400, 200, 400);
      fill(227, 149, 100, 100);
      circle(100,500,400);
      fill(227, 149, 100, 100);
      circle(800,100,400);
    
      // ADD IMAGES
      // image(variable, x, y, width, height);
      image(book1, 100, 100, 200, 350);
      image(book2, 600, 300, 200, 350);
    
      // ADD TEXT + TEXT SIZE + FONTS
      textFont("Courier New");
      textSize(32);
      stroke(201, 138, 56);
      strokeWeight(5);
      fill(82, 50, 10);
      text(
        "“Beware; for I am fearless, and therefore powerful.” — Mary Shelley, Frankenstein",
        153,
        502,
        400
      );
      // ADD EMOJIS
      textSize(100);
      text("🖋️📝📚", 500,200);
    }
    
    ```
    

**In this assignment, you will create an “About Me Collage”** 

Feel free to incorporate images, shapes, colors, or text to your digital collage. 

Consider how:

- Instructions can be clear, in a specific order, and precise to actuate your desired visual output OR unclear, random, and up to chance to produce something unexpected
- Instructions can give meaning to the work outside of the output itself
- Instructions operate in computation and coding, as well as in an art practice

Feel free to:

- Use other photo editing software (ie. Photoshop, Lightroom) to edit images or cut out specific pieces. You can save them as individual PNG files to then digitally collage with.

## Modifications

For K-8: Create a Collage focused only on form and composition of shapes and choice of color palette.  

- Refer to color wheels for color palette inspiration, and focus on getting students to translate a color from the wheel into an R,G,B code value using the help of RGB Color pickers (accessible on Google using Chrome).
- Refer to shape charts to help students understand the relationship of Cartesian coordinate systems to code syntax.

For 9-12: Create an About Me Collage that includes all lessons above. In the provided example, I selected the theme of favorite books. It can be useful to have a “scavenger hunt”-type list to prompt students:

- What is your favorite book? …color? …movie? …emoji? …quote?

## Assessments

As an educator and facilitator, we’re looking for a thorough understanding of:

- **Familiarity of syntax**. An ability to locate bracket pairings and identify the differences between various syntax items
    - Can the student highlight the correct bracket pairings in code? And where to put their code between which brackets?
    - Can the student identify when to use a semicolon? what a function (ie. setup() and draw()) looks like? where the statements or instructions go within functions?
    - Can the student identify how the Cartesian coordinate system relates to the syntax (what we mean by X and Y position)? Or relationships to mathematics (arithmetic and geometry) - ie. diameter for circle, width and height for rectangles, etc.
- Develop a productive workflow
    - Can the student identify where to properly search for help? If it’s a function or code vocab word they don’t know, do they check References? If it’s inspiration, do they check Examples?
    - Can the student refer to the Console Log and utilize it for debugging issues?
    - Can the student set up a desktop environment that helps them best navigate the Web Editor and Reference page? Or, even the desk itself: starting with drawing out their code ideas with pen and paper first?
- Instructional arts
    - Can the student find connections and interesting links between computation and programming with instructional art?