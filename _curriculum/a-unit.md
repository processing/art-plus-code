---
# This is the frontmatter
title: "Topic A: Capturing Movement with Digital Lines" # Title and Heading 1
permalink: /unit-a/ # Give your page a permalink
hidden: false # Remove this line for any units you want added to the sidebar navigation

gallery: # Below is for including an image gallery
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 1 title caption"
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 2 title caption"
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 3 title caption"

---

_A line could also be defined as a dot in motion, or the history of a dot’s movement, since, when we make a continuous mark or a line, we make it by placing a marker point on a surface and moving it along, leaving the formed marks as a record.”_ 
 - Donis A. Dondis, A Primer of Visual Literacy

In many of her drawings, artist Christine Sun Kim captures the motions of sign language through lines. Words like “future” and “time” are depicted with arching curves, mimicking the vertical and horizontal movements of the hand making the sign in ASL. The scale of Kim’s work ranges from intimate drawings to monumental murals. In each of her works, her deliberate choices around the form, weight, and composition of the lines she uses are essential in communicating a unique sense of motion and personality. 

In this topic, we’ll use P5JS to design a unique drawing tool. We’ll design the drawing tool to be compatible with an idea for a drawing. Then we’ll use the tool to create and then save a drawing. 


## References & Artworks for Discussion: Line Quality
* A Primer of Visual Literacy, Donis A. Dondis
* [Art21: Christine Sun Kim](https://art21.org/watch/art-in-the-twenty-first-century/s11/christine-sun-kim-in-friends-strangers/)
* Christine Sun Kim, [Time Owes Me Rest Again](https://queensmuseum.org/exhibition/christine-sun-kim/), 2022, Queens Museum
* Christine Sun Kim, [Too Much Future](https://whitney.org/exhibitions/christine-sun-kim), 2018, Whitney Museum
* Hilma af Klint, [Spiritual Drawing](https://www.guggenheim.org/audio/track/spiritual-drawings-of-the-five-ca-1903-04), ca. 1903, Guggenheim Museum
* Jean-Michel Basquiat, [Untitled](https://www.moma.org/collection/works/34633?artist_id=370&page=1&sov_referrer=artist), 1981, Museum of Modern Art
* Wassily Kandinsky, [Untitled (drawing for Diagram 17)](https://artmuseum.mtholyoke.edu/object/untitled-drawing-diagram-17), 1925, Mount Holyoke College Art Museum
* William Kentridge, [Learning the Flute](https://www.moma.org/collection/works/91559), 2003, Museum of Modern Art
* Elizabeth Peyton, [Craig in Tokyo](https://rubellmuseum.org/elizabeth-peyton), 1997, Rubell Museum


## Objectives
**Art**
- Gaining insight into diverse practices in traditional and contemporary drawing
- Understanding the relationship between drawing tools and artistic intention
- **Visual Arts Vocabulary**: line, space, value, form, texture, color


## Technical Terms & P5JS Elements
- functions [setup()](https://p5js.org/reference/p5/setup/) [draw()](https://p5js.org/reference/p5/draw/)
- canvas methods and variables: [windowWidth](https://p5js.org/reference/p5/windowWidth/), [windowHeight](https://p5js.org/reference/p5/windowHeight/), [background()](https://p5js.org/reference/p5/background/), [frameRate()](https://p5js.org/reference/p5/frameRate/)
- drawing methods: [rect()](https://p5js.org/reference/p5/rect/), [ellipse()](https://p5js.org/reference/p5/ellipse/),  [fill()](https://p5js.org/reference/p5/fill/), [stroke()](https://p5js.org/reference/p5/stroke/), [noStroke()](https://p5js.org/reference/p5/noStroke/)
- mouse variables and methods: [mouseX](https://p5js.org/reference/p5/mouseX/), [mouseY](https://p5js.org/reference/p5/mouseY/), [mouseDragged()](https://p5js.org/reference/p5/mouseDragged/), [doubleClicked()](https://p5js.org/reference/p5/doubleClicked/)
- [save()](https://p5js.org/reference/p5/save/)


## Timeline
This project will take approximately 2-3 45minute sessions:
1. Discussing artists and line, Warm-up Exercises, Introduction to P5JS (Step A1)
2. Creating a drawing tool (A2 - A3), Extending the tool (A4)
3. Finishing the tool (A4), Using the Tool & Sharing Out (Assessment)

### Warm-Up Exercises
Some options for unplugged exercises:
- Blind Contour Drawing
  - Using different drawing utensils (pencil, marker, charcoal, ink) students create blind contour drawings of a single object. Comparing the different drawings, students discuss how the quality of the lines affects the tone and effect of the drawing. 
  - Divide students into pairs and have them create blind contour drawings of each other using different drawing materials. Students discuss how the features of the lines made by different drawing tools supports or doesn’t support the ‘portrait’ of their classmate. 
  - Once the initial P5JS drawing tool is completed, students use the drawing tool they designed to create a blind contour drawing. Compare the drawings with the ones they did using physical materials. Students can then adjust their drawing tool to modify the features. 

- Depicting Movement with Lines
  - Provide students with a simple reference object for drawing (e.g. cube, pencil, eraser) and multiple sheets of paper. For 3 minutes at a time, have random words related to motion (fast, awkwardly, quietly, laboriously) displayed on the board. Have students draw the object moving according to the word on the board.
  - Have students display their work on tables or the board according to the descriptors (e.g. all the quickly drawings on one table). Discuss what are qualities the images have in common for different descriptors. 
  - Students choose one descriptor, and create an intermediate sketch depicting that descriptor. 
  - Students use the P5JS drawing tool to create drawings of the descriptors (or chosen one). Students discuss the difference between digital and physical drawings and compare the drawing experiences.

- Make Your Own Paintbrush
  - Using found materials, students create their own paintbrush. While creating a drawing with their brush, students make observations about the relationship between the shape of their brush and the lines they are creating.
 
### Step A1: Drawing with P5js
[Sample Sketch](https://editor.p5js.org/jyk/sketches/tS5O2kwg9)

Let’s get some code on the board to start fiddling around. When we open the [P5JS web editor](http://editor.p5js.org), we see the following code: 
```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

Our P5JS sketch is divided into 2 sections, function setup() {} and function draw() {}. All of the code between the curly brackets {} after setup() will run once from top to bottom when the page loads. All of the code between the draw() {} curly brackets will repeat.

Let’s modify this code to start drawing. First, we’ll set the size of the canvas to take up the entire width and height of the browser window using the windowWidth and windowHeight variables. windowWidth and windowHeight are examples of variables that come with the P5JS library. We’ll be using a few of these to make our drawing tool. Here, windowWidth is keeping track of the width of the browser, and by using the keyword windowWidth, we are referring to that number. So if the width of your browser window  is 804 and the height of your browser is 476, writing in createCanvas(windowWidth, windowHeight) is the same as writing createCanvas(804, 476). 

Next, we’ll change the color of the background and shape to white using R, G, B values. For commands related to color, we’ll typically use three numbers representing red, green, and blue values. Red, green, and blue are the primary colors for mixing light (positive color system). The maximum value we can put in is 255 and the minimum value is 0.

```js
background(255, 0, 0); 	// 255 red, 0 green, 0 blue makes red
fill(0, 166, 147); 		// 0 red, 166 green, 147 blue makes teal
stroke(228, 204, 255);		// 228 red, 204 green, 255 blue makes lavender
```

We’ll also use the line noStroke() to get rid of the shape’s outline. 

Then we’ll add an ellipse. To draw an ellipse, you set the X position, the Y position, then the width and the height:

```js
function setup() { // this function runs once when the page loads
  createCanvas(windowWidth, windowHeight); // making the dimensions of the canvas take up the entire window
  background(255,255,255); // making the background color white
} // end of the setup() function

function draw() { // this function will loop 60x a second
  background(255,255,255);
  noStroke();
  fill(0,0,0); // fill(r, g, b)
  ellipse(100, 100, 40, 40); // ellipse(x, y, w, h);
}
```

Now you should see a little circle on your white page! Try changing around the numbers so that you can get a sense of what the different components are doing. 

Next, we’ll use the mouseX and mouseY variables. These are like windowWidth and windowHeight except they are used to keep track of the mouse’s X and Y position. 

You can output messages to the console to keep track of changing values like this one:
```js
console.log("your message between these quotation marks");
console.log(nameOfAVariable);
console.log("your message between these quotation marks" + nameOfAVariableNoQuotes
```

Notice how the messages are popping up over and over again in the console with different numbers. This is because the code in the draw function is looping. That means that the command to print a message in the console is being executed again and again and the mouseX and mouseY values are constantly being updated. 

You can also try substituting any of the numbers in the sketch with mouseX and mouseY to see how they might respond to the movement of the mouse.

```js
function draw() { // this function will loop 60x a second
  background(255,255,255);
  noStroke();
  fill(0,0,0);
  console.log("mouse X: " + mouseX); // displaying the mouseX value in the console
  console.log("mouse Y: " + mouseY);
  ellipse(mouseX, mouseY, 40, 40); // making the circle move with the mouse
}
```

### Images

**Images** can be added to the `/assets/images/` directory.

![Soft gradient with pinks and greens]({{ "/assets/images/sample-img.jpg" | relative_url }})

You can also create a `<figure>` element with a caption:

{% include figure popup=true image_path="/assets/images/sample-img.jpg" alt="Soft gradient with pinks and greens" caption="This is a figure caption." %}

You can also create a [gallery of images](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#gallery) (you will need to include the corresponding gallery frontmatter at the top of the page):

{% include gallery caption="This is a sample gallery with **Markdown support**." %}
