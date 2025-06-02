---
# This is the frontmatter
title: "Lost and Found" # Title and Heading 1
permalink: /lostAndFound-lessons/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/curriculum/Unit-1_Sample-2.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-2.gif
    alt: "black circle following a mouse"
    title: "Digital Drawing Tool Step 1"
  - url: /assets/images/curriculum/Unit-1_Sample-3.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-3.gif
    alt: "cursor drawing a black line made up of a series of translucent circles"
    title: "Digital Drawing Tool Step 2"
  - url: /assets/images/curriculum/Unit-1_Sample-4.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-4.gif
    alt: "cursor drawing multiple black arches made up of translucent circles"
    title: "Digital Drawing Tool Step 3"
  - url: /assets/images/curriculum/Unit-1_Sample-5.gif
    image_path: /assets/images/curriculum/Unit-1_Sample-5.gif
    alt: "cursor creating a drawing of vertical blue lines and stamping red ellipses"
    title: "Digital Drawing Tool Step 4"
---
# Lesson Plans & Technical Steps

## 1. Shape
<iframe width="560" height="315" src="https://www.youtube.com/embed/hISICBkFa4Q?si=U-LWuegXM9xtLfXg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

#### 1A. p5.js canvas coordinates
By default, every new p5.js sketch you create on the p5.js Editor will contain the following code:

```jsx
function setup(){
  createCanvas(400,400);
}
```

The [createCanvas()](https://p5js.org/reference/p5/createCanvas/) feature enables you to set the width and height of the canvas. This will determine the physical limit of your drawing surface. Try updating the numbers in between the parentheses in the following sequence, click the Play button, and see what happens:

```jsx
function setup(){
  createCanvas(600,400);
}
```

```jsx
function setup(){
  createCanvas(400,600);
}
```

```jsx
function setup(){
  createCanvas(600,600);
}
```
**Mini-Challenge:** Can you tell which value determines the canvas width and which value determines the canvas height?
{: .notice--warning} 

**Tip:** Similar to the logic of image editing software, you can only create one canvas per sketch. 
Additionally, it’s not possible to animate canvas size while a sketch is playing. 
{: .notice--success}

#### 1B. p5.js coordinate system
We’re on our way to placing shapes on the canvas. Do you recall the Cartesian coordinate system taught in math classes? Don’t worry, we believe this to be much simpler! The p5.js canvas features an invisible coordinate system that originates from an X position of 0 and a Y location of 0 in the top-left corner. 

![p5.js coordinate system]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/coordinates.png?raw=true" | relative_url }}) 

As a shape on the canvas moves to the right of this point, its [X-coordinate value increases](https://editor.p5js.org/Msqcoding/full/AM5ZwrmNo/). As an object on the canvas moves down from this point, its [Y-coordinate value rises](https://editor.p5js.org/Msqcoding/full/jZeTUjZfZ/).

**Code Snippet:** Explore the p5.js coordinate system with this [pixel ruler tool](https://editor.p5js.org/xinemata/sketches/gjWtrowcK) created by Alp Tugǎn, a p5.js Contributor. 
{: .notice--info} 

#### 1C. Drawing simple shapes
Now that we’ve covered the basics of the coordinate system, let’s draw a rectangle on the canvas by using the [rect()](https://p5js.org/reference/p5/rect/) feature!    

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
}

function draw() { 
  background(220); 
  rect(0, 0, 40, 40); // x, y, w, h
}
```  

**Code Snippet:** [Single rect()](https://editor.p5js.org/xinemata/sketches/F71Lv0ddE).
{: .notice--info} 

You should see an adorable white rectangle appearing in the upper-left corner of the canvas. Digging deeper into the syntax of [rect()](https://p5js.org/reference/p5/rect/), we’d learn that within the parentheses, the first number sets the X position; the second number sets the Y position; the third number sets the width; and the fourth number sets the height of the rectangle. 

![p5.js rectangle illustration]({{ "/assets/images/curriculum/Unit-1_Sample-8.png" | relative_url }}) 

Now, add a couple more rectangles to the canvas. You’re invited to experiment with different x, y, width, and height values. Go wild! 

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
}

function draw() { 
  background(220); 
  rect(0, 0, 40, 40); // x, y, w, h
  rect(40, 40, 40, 40); // x, y, w, h
  rect(80, 80, 40, 40); // x, y, w, h
}
```
**Code Snippet:** [Multiple rect()](https://editor.p5js.org/xinemata/sketches/gWHc2OalC).
{: .notice--info} 

**Mini-Challenge:** The example above uses rectangles to form the start of a diagonal line. Can you complete it so that the diagonal line extends across the entire canvas to reach the bottom-right corner?
{: .notice--warning} 

Once you feel more comfortable with drawing rectangles on canvas, we’ll switch over to drawing ellipses using the [ellipse()](https://p5js.org/reference/p5/ellipse/) feature. In coding, it’s always a good idea to start small. So let’s begin by drawing a single ellipse on the canvas:

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
}

function draw() { 
  background(220); 
  ellipse(0, 0, 40, 40); // x, y, w, h
}
```
**Code Snippet:** [Single ellipse()](https://editor.p5js.org/xinemata/sketches/jW_Pq_vCu).
{: .notice--info} 
Hmmm... 🤔 Even though I’m trying to align the ellipse with the upper-left corner by setting X and Y to 0, it’s not behaving as expected. It is as if the edge of the canvas is cutting off the ellipse, and we're only seeing a quarter of the shape. Why is this happening?

It turns out that in computer graphics, rectangles and ellipses have different anchor points:

![rect diagram]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/rect-diagram.png?raw=true" | relative_url }})

The rectangle’s anchor point is on the upper left corner, and the ellipse’s anchor point is in the center of the shape.

![ellipse diagram]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/ellipse-diagram.png?raw=true" | relative_url }}) 

If you want to set the anchor point for ellipses to the upper-left corner, you can add the [ellipseMode()](https://p5js.org/reference/p5/ellipseMode/) feature and set it to CORNER.

![p5.js ellipseMode illustration]({{ "/assets/images/curriculum/Unit-1_Sample-9.png" | relative_url }}) 

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
  ellipseMode(CORNER);
}

function draw() { 
  background(220); 
  ellipse(0, 0, 40, 40); // x, y, w, h
}
```

**Code Snippet:** [ellipseMode()](https://editor.p5js.org/xinemata/sketches/-AxE_NPc-).
{: .notice--info} 

**Tip:** Alternatively, if you want to set the anchor point for rectangles to the center, you can use the [rectMode()](https://p5js.org/reference/p5/rectMode/) feature and set it to CENTER. 
{: .notice--success}

After adding the [ellipseMode()](https://p5js.org/reference/p5/ellipseMode/) feature, your ellipse should be aligned to the upper-left corner. Now, let’s combine this drawing with the rectangle we drew:

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
  ellipseMode(CORNER);
}

function draw() { 
  background(220); 
  ellipse(0, 0, 40, 40); // x, y, w, h
  rect(0, 0, 40, 40); // x, y, w, h
}
```

Something is not quite right. We’ve drawn both [ellipse()](https://p5js.org/reference/p5/ellipse/) and [rect()](https://p5js.org/reference/p5/rect/), but the rectangle is the only visible shape on the canvas. What happens if we switch the order of the [ellipse()](https://p5js.org/reference/p5/ellipse/) and [rect()](https://p5js.org/reference/p5/rect/) code?

```jsx
function setup() {  
  createCanvas(400, 400); // w, h
  ellipseMode(CORNER);
}

function draw() { 
  background(220); 
  rect(0, 0, 40, 40); // x, y, w, h
  ellipse(0, 0, 40, 40); // x, y, w, h
}
```

**Code Snippet:** [ellipse() + rect()](https://editor.p5js.org/xinemata/sketches/29C52nZDz).
{: .notice--info} 

The ellipse should now be sitting on top of your rectangle. What this tells us is that the order in which you code your shapes matters. [p5.js](https://p5js.org) is built on JavaScript, and JavaScript renders code on the fly from top to bottom. Coding the rectangle first means that the rectangle is drawn first, and then it gets covered by the ellipse, which comes later. 

### 2. Color
<iframe width="560" height="315" src="https://www.youtube.com/embed/fTEvHLLwSBE?si=O-3UMF0ZjaUhQb6M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

#### Grade 6~8
##### 2A. Story Behind the Screen
Look at the screen in front of you right now. Every color you see—bright pinks, glowing greens, stormy blues—is made from just three colors of light: red, green, and blue—also known as RGB.

You can’t always see it, but it’s true. If you looked at your phone or computer screen under a microscope (cool science class moment!), you’d see tiny red, green, and blue lights—called pixels—turning on and off in different combinations. That’s how screens make color: by mixing light.

![RGB screen]({{ "https://upload.wikimedia.org/wikipedia/commons/9/9d/TFT_Bildschirm_RGB_Pixel.JPG" | relative_url }}) 

This kind of color mixing is called additive color. It’s different from mixing paint, where adding more makes things darker. With light, adding more actually make things brighter.

![RGB mixing]({{ "https://upload.wikimedia.org/wikipedia/commons/5/59/RGB_combination_on_wall.png" | relative_url }}) 


In this topic, we'll learn to cast some color spells together using code. You’ll learn how to control the RGB colors in p5.js, a creative coding environment made for artists, designers, and anyone curious about how code can be expressive.

##### 2B. Meet RGB

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

Play around! What happens with:
- `background(255, 255, 255)`?
- `background(0, 0, 0)`?

**Tip**: If you only type one number like `background(150)`, it fills the background with a shade of gray. That’s a shortcut for `background(150, 150, 150)`.
{: .notice--success} 

---

##### 2C. Filling Shapes with Color

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
**Code Snippet:** [fill()](https://editor.p5js.org/xinemata/sketches/sU7-2LedO).
{: .notice--info} 

Once you feel comfortable with using RGB colors, you have the option of going further by adding a fourth number to [fill()](https://editor.p5js.org/xinemata/sketches/sU7-2LedO)  to make something see-through!

```js
fill(255, 0, 0, 100);  // r, g, b, alpha
```

The last number is called the alpha value. It also ranges from 0 (fully transparent) to 255 (fully opaque).

**Mini-Challenge:** Try overlapping shapes with different alpha values. What kinds of layering effects can you make?
{: .notice--warning} 

##### 2D. Draw your favorite snack
Let’s use everything you’ve learned so far to draw a snack you love. Think about ways you could represent your snack using 2D primitives like ellipses and rectangles. And instead of guessing the RGB values of a color you want to use, play around with this [color picker](https://g.co/kgs/6fssxMC) to choose specific colors. Below is an example of a lollipop:

![lollipop made in p5.js]({{ "/assets/images/curriculum/Unit-1_Sample-10.png" | relative_url }}) 

**Code Snippet:** [lollipop example](https://editor.p5js.org/xinemata/sketches/reojWdPOp).
{: .notice--info} 

**Tip:** Adding [noStroke()](https://p5js.org/reference/p5/noStroke/) removes the black outline around shapes. [stroke()](https://p5js.org/reference/p5/stroke/) sets the outline to a different color. [strokeWeight()](https://p5js.org/reference/p5/strokeWeight/) alters the thickness of the outline.
{: .notice--success} 

#### Grade 9~12
##### 3. Blend Modes

Want your colors to mix in cool ways—like in Photoshop or Instagram filters? Try this:

```js
function setup() {
  createCanvas(400, 400);
  blendMode(LIGHTEST);  // Try other modes: DARKEST, MULTIPLY, DIFFERENCE

  fill(255, 0, 0);
  ellipse(150, 200, 200, 200);

  fill(0, 0, 255);
  ellipse(250, 200, 200, 200);
}
```

Blend modes change how colors mix when they overlap. Each one creates different visual effects.