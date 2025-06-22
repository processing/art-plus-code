---
# This is the frontmatter

title: "Mask Generator" # Title and Heading 1
permalink: /maskGenerator-intro/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/thumbnails/unit2.png
    image_path: /assets/images/thumbnails/unit2.png
    alt: "Screenshot of a collage on books using the p5.js web editor"
    title: "About Me Collage"
---

![Create a digital collage with p5.js!]({{ "https://verse.works/image/w3840/static%2F1dbce05a-42de-4250-a1b7-4f22d3e61886.png@webp" | relative_url }})  
[Generativemasks](https://generativemasks.io/gallery). Made in [p5.js](https://p5js.org/) by Shunsuke Takawo.

# Introduction

> ‍I write code as though I’m improvising with a musical instrument — for me, sketching has become like humming a melody.
>
> \- Shunsuke Takawo, Right Click Save

In [parameterized design](https://formandcode.com/code-examples/parameterize-chair), you are a conductor, not just one musician. Instead of creating a single design by drawing every detail step-by-step, you use code to set up rules (called parameters) that can create many different versions of a design.

Kabuki theater in Japan uses expressive masks to show different roles in society. For this topic, you will reflect on your own background and design a “mask generator” using customized variables and the [random()](https://p5js.org/reference/p5/random/) feature. 

The generator will use mouse or keyboard interactions to create different versions of your mask. Test it, make changes, and pay close attention to the details as you improve your design.

## Premise

Build a simple generator that makes multiple variations of the same mask.

## Learning Objectives

### Grade 6~8

- Create clearly named variables that store data, and perform operations on their contents.
- Test and analyze the effects of changing variables while using computational models.
- Decompose problems and subproblems into parts to facilitate the design, implementation, and review of programs.
- Discuss issues of bias and accessibility in the design of existing technologies.
- Hands-on experience with variable scope.

### Grade 9~12

- Study, discuss, and think critically about the potential impacts and implications of emerging technologies
  on larger social, economic, and political structures, with evidence from credible sources.
- Compare levels of abstraction and interactions between application software, system software, and hardware.

## Technical Terms & p5.js Elements

### Grade 6~8

- System Variables vs. User-Defined Variables
- [mouseX](https://p5js.org/reference/p5/mouseX/), [mouseY](https://p5js.org/reference/p5/mouseY/)
- [width](https://p5js.org/reference/p5/width/), [height](https://p5js.org/reference/p5/height/)
- Data types
- Global vs. local variables
- [random()](https://p5js.org/reference/p5/random/)
- [mousePressed()](https://p5js.org/reference/p5/mousePressed/), [keyPressed()](https://p5js.org/reference/p5/keyPressed/)
- console.log()

### Grade 9~12

- Iterative design

## Timeline

This project will take approximately four 45-minute sessions:

1. Discussing art references and warm-up cxercise.
1. Designing the mask generator.
1. Coding the mask generator in p5.js.
1. Making iterations as needed. Sharing out.

## Warm-Up Exercises

### Planning your Mask Generator Project

1. Draw Your Grid
- Use your paper and pencil to draw a large square (around 4x4 inches).
- Divide the square into a 20 x 20 grid with a ruler.
- This will help you keep things lined up and make variations easier to compare.

1. Create Two Key Expressions
   - Using the [Wheel of Emotions](<https://www.isu.edu/media/libraries/counseling-and-testing/documents/Wheel-of-Emotions-Handout-(3).pdf>) as a reference and select two types of emotional expressions.
   - In the first square, draw a mask showing Expression 1 (e.g., inspired, courageous, respected).
   - In the second square, draw the same face showing Expression 2 (e.g., worried, overwhelmed, alienated).

1. Keep the features the same, but change features like:
   - Eyes: big, small, squinted
   - Mouth: smiling, frowning, open, closed
   - Eyebrows: raised, tilted, flat

1. Design the In-Between Faces
   - Now, imagine how the mask moves from the first expression to the second.
   - On a new piece of paper, draw 2–3 versions that mix parts of each expression. For example: a mask that’s just starting to frown, or eyes that are half-closed.
1. Observe & Reflect
   - Compare your key expressions:
     - What changes the most between expressions?
     - Which parts stay mostly the same?
     - What combinations feel natural or interesting?
