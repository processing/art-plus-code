---
# This is the frontmatter
title: "Mask Generator" # Title and Heading 1
permalink: /maskGenerator-lessons/3 # Give your page a permalink
published: true
---

Mask Generator remixes Critical Computation by Xin Xin and Katherine Moriwaki, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en)

## Mouse and Keyboard Interaction

### Grade 6~8

#### Mouse Interaction

This section introduces [mousePressed()](https://p5js.org/reference/p5/mousePressed/). With this feature, you can use the mouse button to generate a new random number everytime the mouse is pressed:

```js
let d;

function setup() {
  createCanvas(400, 400);
  d = random(80, 100); // randomly pick a number between 80 and 100
}

function draw() {
  background(220);
  ellipse(200, 200, d, d);
}

function mousePressed(){
  d = random(80, 100); // randomly pick a number between 80 and 100
  console.log(d); // print d
}
```

 ![Random circle]({{ "/assets/images/curriculum/Unit-2_Sample-10.gif" | relative_url }}) 

Let's get more practice by applying the same idea to the [lollipop example](https://editor.p5js.org/xinemata/sketches/reojWdPOp). Update the sketch so that everytime mouse is pressed, the candy will get assigned a new random color.  

```js
function draw() {
  background(220);

  //Lollipop stick
  fill(255);
  rect(stickX, stickY, stickWidth, stickHeight);

  //Lollipop candy
  fill(candyR, candyG, candyB);
  ellipse(candyX, candyY, candyWidth, candyHeight);
}

function mousePressed() {
  candyR = random(0, 255); // randomly pick a number between 0 and 255
  candyG = random(0, 255); // randomly pick a number between 0 and 255
  candyB = random(0, 255); // randomly pick a number between 0 and 255
  console.log(candyR, candyG, candyB); // print candyR, candyG, candyB
}
```

 ![Random circle]({{ "/assets/images/curriculum/Unit-2_Sample-11.gif" | relative_url }}) 

**Code Snippet:** [random lollipop example](https://editor.p5js.org/xinemata/sketches/IG9-aEdGT).
{: .notice--info}

**Tip:** Code inside of `function mousePressed()` runs once after the mouse button gets pressed.
{: .notice--success}

#### Keyboard Interaction

[keyPressed()](https://p5js.org/reference/p5/keyPressed/) works in a very similar way. With this feature, you can run a block of code after any key on the keyboard gets pressed. 

```js
let d;

function setup() {
  createCanvas(400, 400);
  d = random(80, 100); // randomly pick a number between 80 and 100
}

function draw() {
  background(220);
  ellipse(200, 200, d, d);
}

function keyPressed(){
  d = random(80, 100); // randomly pick a number between 80 and 100
  console.log(d); // print d
}
```

Now that you've learned the basics of mouse and keyboard interactions, incorporate this feature into your Mask Generator to give your audience more control over the interactive experience. 