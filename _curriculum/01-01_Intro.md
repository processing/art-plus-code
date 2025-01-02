---
# This is the frontmatter
title: "Capturing Movement with Digital Lines: Introduction & Inspiration" # Title and Heading 1
permalink: /capturingMovement-intro/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: 
    image_path: https://whitneymedia.org/assets/artwork/60038/2018_183_cropped.jpeg
    alt: "black and white abstract drawing of curves with handwritten text: too much future "
    title: "Christine Sun Kim, Too Much Future, 2018 (Whitney Museum)"
  - url: /assets/images/unit_a_example-2.png
    image_path: /assets/images/unit_a_example-2.png
    alt: "simplified line drawing of a face with red oval pattern"
    title: "Sample Drawing 2"

---

# Capturing Movement with Digital Lines

> A line could also be defined as a dot in motion, or the history of a dot’s movement, since, when we make a continuous mark or a line, we make it by placing a marker point on a surface and moving it along, leaving the formed marks as a record.” 
>
> \- Donis A. Dondis, A Primer of Visual Literacy

In many of her drawings, artist Christine Sun Kim captures the motions of sign language through lines. Words like “future” and “time” are depicted with arching curves, mimicking the vertical and horizontal movements of the hand making the sign in ASL. The scale of Kim’s work ranges from intimate drawings to monumental murals. In each of her works, her deliberate choices around the form, weight, and composition of the lines she uses are essential in communicating a unique sense of motion and personality. 

In this topic, we’ll use P5JS to design a unique drawing tool. We’ll design the drawing tool to be compatible with an idea for a drawing. Then we’ll use the tool to create and then save a drawing. 

{% include gallery caption="Create your own drawing tool using P5JS!" %}

## Objectives
- Gaining insight into diverse practices in traditional and contemporary drawing
- Understanding the relationship between drawing tools and artistic intention
- **Visual Arts Vocabulary**: line, space, value, form, texture, color


## Technical Terms & P5JS Elements
- functions: [setup()](https://p5js.org/reference/p5/setup/), [draw()](https://p5js.org/reference/p5/draw/)
- canvas methods and variables: [windowWidth](https://p5js.org/reference/p5/windowWidth/), [windowHeight](https://p5js.org/reference/p5/windowHeight/), [background()](https://p5js.org/reference/p5/background/), [frameRate()](https://p5js.org/reference/p5/frameRate/)
- drawing methods: [rect()](https://p5js.org/reference/p5/rect/), [ellipse()](https://p5js.org/reference/p5/ellipse/),  [fill()](https://p5js.org/reference/p5/fill/), [stroke()](https://p5js.org/reference/p5/stroke/), [noStroke()](https://p5js.org/reference/p5/noStroke/)
- mouse variables and methods: [mouseX](https://p5js.org/reference/p5/mouseX/), [mouseY](https://p5js.org/reference/p5/mouseY/), [mouseDragged()](https://p5js.org/reference/p5/mouseDragged/), [doubleClicked()](https://p5js.org/reference/p5/doubleClicked/)
- [save()](https://p5js.org/reference/p5/save/)
- console.log()


## References & Artworks for Discussion: Line Quality
{% include gallery%}
* A Primer of Visual Literacy, Donis A. Dondis
* [Art21: Christine Sun Kim](https://art21.org/watch/art-in-the-twenty-first-century/s11/christine-sun-kim-in-friends-strangers/)
* Christine Sun Kim, [Time Owes Me Rest Again](https://queensmuseum.org/exhibition/christine-sun-kim/), 2022, Queens Museum
* Christine Sun Kim, [Too Much Future](https://whitney.org/exhibitions/christine-sun-kim), 2018, Whitney Museum
* Hilma af Klint, [Spiritual Drawing](https://www.guggenheim.org/audio/track/spiritual-drawings-of-the-five-ca-1903-04), ca. 1903, Guggenheim Museum
* Jean-Michel Basquiat, [Untitled](https://www.moma.org/collection/works/34633?artist_id=370&page=1&sov_referrer=artist), 1981, Museum of Modern Art
* Wassily Kandinsky, [Untitled (drawing for Diagram 17)](https://artmuseum.mtholyoke.edu/object/untitled-drawing-diagram-17), 1925, Mount Holyoke College Art Museum
* William Kentridge, [Learning the Flute](https://www.moma.org/collection/works/91559), 2003, Museum of Modern Art
* Elizabeth Peyton, [Craig in Tokyo](https://rubellmuseum.org/elizabeth-peyton), 1997, Rubell Museum


## Timeline
This project will take approximately two to three 45minute sessions:
1. Discussing artists and line, Warm-up Exercises, Introduction to P5JS
2. Creating a drawing tool, Extending the tool
3. Finishing the tool, Using the Tool & Sharing Out (Assessment)


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
