---
# This is the frontmatter
title: "A Walk in the Neighborhood" # Title and Heading 1
permalink: /walkInNeighborhood-lessons/3 # Give your page a permalink
published: true
---

## Walk in the Neighborhood Project

### **Step-by-Step Guide to Building your Project**

##### Step 1: Set Up Your Project

1. Open editor.p5js.org
2. Click "New Sketch"
3. Create a folder on your computer with these 4 files:
   - **1.png** (left-facing image)
   - **2.png** (front/up/down image)
   - **3.png** (right-facing image)
   - **map.jpg** (background map image)

In the p5 editor, go to the "Sketch Files" panel and upload all 4 images.

##### Step 2: Write the Code

**A. Create variables to hold your images and character position**

```js
let bg;
let frame1;
let frame2;
let frame3;

let x = 300;
let y = 300;
```

- `bg` will hold your background map.
- `frame1`, `frame2`, and `frame3` are character images facing different directions.
- `x` and `y` store the position of your character on the canvas.

**B. Define a target location for your character to interact with**

```js
let targetX = 200;
let targetY = 200;
```

- This is the location you want your character to “find” (like a mailbox or building).
- Later, we’ll use the `dist()` function to check how close the character is to this spot.

**C. Load your images with await `loadImage()` in an `async` setup function**

```js
async function setup() {
  frame1 = await loadImage("1.png"); // left-facing
  frame2 = await loadImage("2.png"); // front/up/down
  frame3 = await loadImage("3.png"); // right-facing
  bg = await loadImage("map.jpg");

  createCanvas(800, 600);
}
```

- `await loadImage()` tells the computer to wait for the image to fully load before moving on.
- This avoids errors where the program tries to draw an image that hasn’t finished loading.
- `createCanvas(800, 600)` makes a canvas that matches the size of your map. Change these numbers so they fit your "map.jpg" asset.

**D. Set up the main drawing loop**

```js
function draw() {
  imageMode(CORNER);
  background(bg);
```

- `draw()` runs over and over (about 60 times per second).
- `background(bg)` displays your map image each time to “clear” the previous frame.
- `imageMode(CORNER)` tells p5 to draw the background image from the top-left corner.

**E. Use the dist() function to measure how close the character is to something**

```js
let d = dist(x, y, targetX, targetY);
```

- dist() means distance. It tells us how far apart two points are.
- x, y is your character’s current position.
- targetX, targetY is where the special location (like a mailbox) is.
- The result is stored in a variable called d.

**Example**
If `d < 50`, that means your character is within 50 pixels of the target. That's close enough to trigger an event!

```js
if (d < 50) {
  fill(0);
  textSize(24);
  text("You have mail!", x - 50, y + 60);
}
```

**F. Move the character and change direction based on arrow keys**

```js
imageMode(CENTER);

if (keyIsPressed) {
  if (key == RIGHT_ARROW) {
    image(frame3, x, y, frame3.width / 5, frame3.height / 5);
    x = +1;
  }
  if (key == LEFT_ARROW) {
    image(frame1, x, y, frame1.width / 5, frame1.height / 5);
    x = -1;
  }
  if (key == UP_ARROW) {
    image(frame2, x, y, frame2.width / 5, frame2.height / 5);
    y = -1;
  }
  if (key == DOWN_ARROW) {
    image(frame2, x, y, frame2.width / 5, frame2.height / 5);
    y = +1;
  }
} else {
  image(frame2, x, y, frame2.width / 5, frame2.height / 5);
}
```

**Let's break this down:**

- **`imageMode(CENTER)`**: Draws your character centered on x, y
- **`keyIsPressed`**: Checks if any key is currently being pressed
- **`key == RIGHT_ARROW`**: Only true if the right arrow key is pressed
- **`image(...)`**: Draws the correct image facing the right way
- **`x += 2, y -= 2,` etc.**: Moves your character on the screen

##### Step 3: Test it out!

- Use the arrow keys to move your character around.
- Walk toward the target spot (`targetX`, `targetY`) to see the message appear.
- Change the values of `targetX` and `targetY` to move the location.

> Challenge
> Add at least two more points on your map that your character can interact with.
> Code Snippet: [Neighborhood Example](https://editor.p5js.org/xinemata/sketches/eMkk3Zub_).
