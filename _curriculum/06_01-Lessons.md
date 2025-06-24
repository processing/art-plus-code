---
# This is the frontmatter
title: "A Walk in the Neighborhood" # Title and Heading 1
permalink: /walkInNeighborhood-lessons/1 # Give your page a permalink
published: true

---

## Loading and Displaying Images

### Grade 6~8

#### Uploading an Image

- First and foremost, let's switch over to the latest version of p5.js on the p5.js Editor!
- Find an image for your project or start with this [picture of a cat](/assets/images/curriculum/cat_front.png);
- Open the p5.js Editor and select the arrow next to sketch.js on the top left of the Editor. The sketch folder will appear on the left sidebar.
Click the plus “+” button, and select “Upload file”.
- Select the image from your device and upload them into the sketch folder. You can drag and drop the files into the upload box that appears, or click the box and select files from your computers’ files manager.

![Upload image in editor]({{ "https://beta.p5js.org/_astro/upload-editor-files.CM5V5Y2t_2d2r5R.webp" | relative_url }})

**Tip:** p5.js Editor accepts images with `.jpg`, `.png`, `.gif` extensions.
{: .notice--success}

**Tip:** `.png` support images with transparent backgrounds, while `.gif` contains a series of images that can be displayed as an animation.
{: .notice--success}

#### Loading an Image

In order to load an image, you will first need to create an **empty variable**, then store the image using [loadImage()](https://beta.p5js.org/reference/p5/loadimage/):

```js
let catFront; // create a variable to store the image

async function setup() {
  catFront = await loadImage("cat_front.png"); // load the image into catFront
  createCanvas(400, 400);
  imageMode(CENTER); // Shifts image anchor point to the center
}
```
**Tip:** Using `async` and `await` ensures that your image completes loading before the program continues to run.
{: .notice--success}


#### Displaying Image

To display the image, move over to `function draw()` and apply the [image()](https://beta.p5js.org/reference/p5/image/) feature:

```js
function draw() {
  background(220);
  image(catFront, x, y, 100, 100); // variable name, x, y, w, h
}
```

![Cat sitting]({{ "/assets/images/curriculum/catSitting.png" | relative_url }}) 

If you don't have a square image, the approach above might have distorted your image. To avoid distortion, use `catFront.width` and `catFont.height` to access the width and height values of your uploaded image:

```js
let catFront; // create a variable to store the image

async function setup() {
  catFront = await loadImage("cat_front.png"); // load the image into catFront
  createCanvas(400, 400);
  imageMode(CENTER); // Shifts image anchor point to the center
  console.log(catFront.width, catFront.height); // width and height of the uploaded image
}
```

Then you can use division to cut the width and height of an image down at the same ratio:

```js
function draw() {
  background(220);
  image(catFront, x, y, catFront.width / 5, catFront.height / 5); // variable name, x, y, w, h
}
```

**Code Snippet:** [cat sitting image](https://editor.p5js.org/xinemata/sketches/p6zkCLnvU).
{: .notice--info}