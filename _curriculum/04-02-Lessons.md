---
# This is the frontmatter
title: "Mask Generator" # Title and Heading 1
permalink: /maskGenerator-lessons/2 # Give your page a permalink
published: true
---
## Randomness

### Grade 6~8

#### Empty Variables

So far, we've been naming variables and storing data in them all in one go. But there's actually a way to create a variable, name it, and not store data inside until later. This type of variable is called an **empty variable**. 

```js
let d; // create an empty variable

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  d = 100; // assign 100 to d
  ellipse(200, 200, d, d);
  console.log(d); // print d
}
```
Why would we need to wait to store data inside of an **empty variable**? One possible reason is because we're generating a random number, and that number won't get created until `function draw()` runs. 

#### Creating a Random Number

[random()](https://p5js.org/reference/p5/random/) is a [p5.js](https://p5js.org/) feature that generates a random number between a minimum value and a maximum value:

```js
let d; // create an empty variable

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  d = random(80, 100); // generates a random number between 80 and 100
  ellipse(200, 200, d, d);
  console.log(d); // print d
}
```

Because `function draw()` runs 60 times per second, the code above would generate 60 new random numbers between 0 and 3 every second. 

 ![Random circle]({{ "/assets/images/curriculum/Unit-2_Sample-9.gif" | relative_url }}) 

 What if we can modify this sketch, so that only when you press your mouse button, a new random number gets generated?