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

**Tips:** Similar to the logic of image editing software, you can only create one canvas per sketch. 
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

**Tips:** Alternatively, if you want to set the anchor point for rectangles to the center, you can use the [rectMode()](https://p5js.org/reference/p5/rectMode/) feature and set it to CENTER. 
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