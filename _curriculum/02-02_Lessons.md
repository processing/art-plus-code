---
# This is the frontmatter
title: "Lost and Found" # Title and Heading 1
permalink: /lostAndFound-lessons/2 # Give your page a permalink
published: true
---

## Color
<iframe width="560" height="315" src="https://www.youtube.com/embed/fTEvHLLwSBE?si=O-3UMF0ZjaUhQb6M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Grade 6~8
#### A. Story Behind the Screen
Look at the screen in front of you right now. Every color you see—bright pinks, glowing greens, stormy blues—is made from just three colors of light: red, green, and blue—also known as RGB.

You can’t always see it, but it’s true. If you looked at your phone or computer screen under a microscope (cool science class moment!), you’d see tiny red, green, and blue lights—called pixels—turning on and off in different combinations. That’s how screens make color: by mixing light.

![RGB screen]({{ "https://upload.wikimedia.org/wikipedia/commons/9/9d/TFT_Bildschirm_RGB_Pixel.JPG" | relative_url }}) 

This kind of color mixing is called additive color. It’s different from mixing paint, where adding more makes things darker. With light, adding more actually make things brighter.

![RGB mixing]({{ "https://upload.wikimedia.org/wikipedia/commons/5/59/RGB_combination_on_wall.png" | relative_url }}) 


In this topic, we'll learn to cast some color spells together using code. You’ll learn how to control the RGB colors in p5.js, a creative coding environment made for artists, designers, and anyone curious about how code can be expressive.

#### B. Meet RGB

Let’s start by updating the [background()](https://p5js.org/reference/p5/background/) in the [p5.js editor](https://editor.p5js.org/):

```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(255, 0, 0);  // r, g, b
}
```

If you click the Play button, the background of the canvas should be filled in bright red. Let's break this down to better understand what's going on:

- RGB ranges from a minimum value of 0, to a maximum value of 255. These numbers control the brightness levels of the red, green, and blue lights. 
- In this case, the sketch is coloring the background in the brightest possible red in RGB. `background(255, 0, 0);` means: full red light, no green light, and no blue light. 

**Mini-Challenge:** Can you update background() to fill the canvas with the brightest blue possible?
{: .notice--warning} 

**Tip**: In the RGB world, `background(255, 255, 0);` creates yellow, `background(255, 0, 255);` creates magenta, and `background(0, 255, 255);` creates cyan.
{: .notice--success} 

Play around! What happens when you assign the same number to R, G, B?
- `background(255, 255, 255)` will make the background white
- `background(0, 0, 0)` will make the background black
- `background(150, 150, 150)` will make the background light grey

Assigning the same number to R, G, B creates a color on the grayscale. 

**Tip**: `background(255)` is the short-hand way of writing `background(255, 255, 255)`. This saves you the trouble of having to type the same number into [background()](https://p5js.org/reference/p5/background/) three times.
{: .notice--success} 

---

#### C. Filling Shapes with Color

Let’s add an ellipse and give it color using the [fill()](https://p5js.org/reference/p5/fill/) feature:

```js
function setup() {  
  createCanvas(400, 400); // w, h
  rectMode(CENTER);
}

function draw() { 
  background(220); 
  fill(255, 255, 0); // r, g, b
  rect(200, 200, 40, 40); // x, y, w, h
  ellipse(200, 200, 40, 40); // x, y, w, h
}
```

By default, [fill()](https://p5js.org/reference/p5/fill/) recognizes RGB values and sets the color of the shapes you draw. But what if you want to fill the ellipse with a different color? You will need to place another [fill()](https://p5js.org/reference/p5/fill/) right before the ellipse. 

```js
function setup() {  
  createCanvas(400, 400); // w, h
  rectMode(CENTER);
}

function draw() { 
  background(220); 
  fill(255,255,0); // r, g, b
  rect(200, 200, 40, 40); // x, y, w, h
  fill(255,0,255); // r, g, b
  ellipse(200, 200, 40, 40); // x, y, w, h
}
```
**Code Snippet:** [fill() example](https://editor.p5js.org/xinemata/sketches/sU7-2LedO).
{: .notice--info} 

Once you feel comfortable with using RGB colors, you have the option of going further by adding a fourth number to [fill()](https://editor.p5js.org/xinemata/sketches/sU7-2LedO)  to make something see-through!

```js
fill(255, 0, 0, 100);  // r, g, b, alpha
```

The last number is called the alpha value. It also ranges from 0 (fully transparent) to 255 (fully opaque).

**Mini-Challenge:** Try overlapping shapes with different alpha values. What kinds of layering effects can you make?
{: .notice--warning} 

#### D. Draw your favorite snack
Let’s use everything you’ve learned so far to draw a snack you love. Think about ways you could represent your snack using 2D primitives like ellipses and rectangles. And instead of guessing the RGB values of a color you want to use, play around with this [color picker](https://g.co/kgs/6fssxMC) to choose specific colors. Below is an example of a lollipop:

![lollipop made in p5.js]({{ "/assets/images/curriculum/Unit-1_Sample-10.png" | relative_url }}) 

**Code Snippet:** [lollipop example](https://editor.p5js.org/xinemata/sketches/reojWdPOp).
{: .notice--info} 

**Tip:** Adding [noStroke()](https://p5js.org/reference/p5/noStroke/) removes the black outline around shapes. [stroke()](https://p5js.org/reference/p5/stroke/) sets the outline to a different color. [strokeWeight()](https://p5js.org/reference/p5/strokeWeight/) alters the thickness of the outline.
{: .notice--success} 

### Grade 9~12
#### E. Color Modes

Color scientists create color models such as RGB to describe colors. Color models contain mathematical rules. For example, RGB can only be expressed between 0 and 255. 

Beyond RGB, there are many other [colorMode()](https://p5js.org/reference/p5/colorMode/) you could use in p5.js. For instance, HSB standing for hue, saturation, and brightness, is a color model that can make coloring more intuitive. 

![RGB to HSB diagram 1]({{ "/assets/images/curriculum/RGB-HSB_0.jpg" | relative_url }}) 

You can draw the exact same color in both RGB and HSB modes, except you'd describe them differently because they follow different mathematical rules. 

```js
function setup() {  
  createCanvas(400, 400); // w, h
  rectMode(CENTER);
}

function draw() { 
  background(220); 
  // Set color to yellow in RGB
  colorMode(RGB);
  fill(255,255,0); // r, g, b
  rect(200, 200, 40, 40); // x, y, w, h
  // Set color to yellow in HSB
  colorMode(HSB);
  fill(60, 100, 100); // h, s, b
  ellipse(200, 200, 40, 40); // x, y, w, h
}
```
**Code Snippet:** [colorMode() example](https://editor.p5js.org/xinemata/sketches/q3XUTPjJD).
{: .notice--info} 