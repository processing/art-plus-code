---
title:  "Coding Collage: Exploring self, place, and space in digital art"
author: Jennie Canning
date:   2024-12-18 00:00:00 -0400
published: true

header:
  teaser: /assets/images/resources/jennie-canning/resource-thumbnail.png
excerpt: "An interactive collage inspired by Romare Bearden to explore connections to community using images, shapes and audience interactions. "
---

## Introduction/Overview
![Sample code and image of an interactive collage project in p5.js]({{ "assets/images/resources/jennie-canning/Sample_JennieC_Collage.png" | relative_url }})  

Students will look at who they are in connection to their community. Taking inspiration for one of Pittsburgh’s most notable artist, Romare Bearden, they will explore ways to show their place in their community be it a neighborhood, a family, a street, or their school.  Students will take pictures, find images, and create shapes to create a digital collage in p5.js. After the collage has been created, we will explore ways to invite audience reaction through interactions that have been created in p5.js like the drawing tools, changing objects appearance based on the mouse positioning, and typing with the keyboard. Students will get a chance to reflect on how the audience has changed their piece through the interactions.

- [Full lesson](https://docs.google.com/document/d/1dpokQdBL041a1g545nvVG9Kwu1tM5qwCXXTWxMhQ-HE/edit?usp=sharing)

**Example completed sketches:** [Neighbourhood](https://editor.p5js.org/canning.jennie/sketches/Z8tjurPJ2)
{: .notice--info}

## Learning Audience

This lesson plan is specifically for high school students in a STEAM class. They have not had previous JavaScript experience. Some might have had block based coding experience. 

This lesson can be modified for visual art teachers by making the collage on paper, and just the interactions in p5.js or used as an introduction by just doing the collage. 

More advanced STEAM classes could incorporate dragging and placing interactions. 

## Established Goals

1. Students will look at Romare Bearden’s work, reflect and discuss social themes that were prevalent during the Harlem Renaissance period and compare and contrast to social themes today and their community.  
2. Students will create a self-portrait in mixed media incorporating their own symbol set.    
3. Students will explore cultural and personal symbols and identify ones that represent themselves, their community, and a time period  
4. Students will use technology as a media resource to create images that allow for audience interaction.   
5. Students will reflect upon the process.

## Objectives

- **What work will students complete?**
  * Students will create a digital collage with at least one type of interaction.
- **What information will students *know* at the end of this project/lesson?**
  * Different cultures and subcultures interpret images and symbols differently.   
  * Images, color and style can depict an idea, emotion, or tone.   
  * The creation process has many steps.   
  * Audience interprets the meaning of a work of art based on their own personal experiences.   
  * Artist can use  p5.js to create a collage using images, shapes, and colors that allows for viewer participation  
- **What new *skills* will students gain (or practice)?**
  * Students will be introduced to p5.js, learn the following:  
  * Loading images and placing them on the grid  
  * Drawing shapes on the grid; rect, and ellipse, triangle, line  
  * Changing colors  
  * Interactions   
- **Will the students have new understandings or questions after this project/lesson?**
  * Students will understand that…  
    + Different cultures and subcultures understand their own symbols.  
    + Artist choose specific symbolism in their artwork to convey a message to the audience.  
    + Technology can be used to express ideas.    
    + Audience interprets the meaning of a work of art based on their experience with the work.   
  * Students will most likely have many questions about how to integrate technology into works are art   
- **Are there options for differentiation?**
  * Scaffolding can be created where a sketch is shared with a grid on it to help students place objects.   
  * Only shapes can be used instead of images to simplify the coding.  
  * Collages can first be created out of paper and then manipulated  digitally to create the different part of the collage that the user can manipulate. 

## Technical Terms & p5.js Elements

- Code syntax
- createCanvas(w, h);
- circle(x, y, d);
- ellipse(x, y, w, h);
- rect(x, y, w, h);
- line(x1, y1, x2, y2);
- Conditional Statement
- if-then, if-then-else, else if
- Mouse
- Right click, left click
- Keys & Keyboard

## Visual Arts Vocabulary

- Color scheme
- Tone
- Emphasis
- Contrast
- Form
- Space
- Symbolism
- Audience

## External References & Resources

- [Romare Bearden's Artwork](https://beardenfoundation.org/art/)
- [Art+Code: Instructional Art](https://processing.github.io/art-plus-code/instructionalArt-Intro/)
- [Art+Code: Interactive Art](https://processing.github.io/art-plus-code/interactiveArt-Intro/)

## Learning Plan

### Day 1 Activities

**Focus of the day:** Identifying Symbolism 
- How do we decode symbols?
- How are symbols used in artwork?

**How will you know that students are getting it?**
- Students can articulate through image analysis the symbolism in artwork.

**How does the essential question connect students to this day’s focus?**
- Decoding symbolism in other artist work will help students begin to their own personal and cultural symbols.  

#### Process
**Warm Up:** 5 min Quick write - What are Symbols?  Where do they come from?  Share out as a group charting different symbols sets.

**Group Work:** Image Analysis of Romare Bearden’s collages , divide class into groups of 4.  Each group will complete the image analysis of their assigned image.  Gallery walk of image analysis.  Other groups can add or questions using stickies the other groups findings. Share out.

**Brainstorm:** Each student begins to brainstorm their own symbols that represent themselves and their community. Remind them that symbolism can be colors, shapes, styles, not just concrete symbols.

**Wrap Up:** Share out Personal symbolism and add to the class symbol charts.  

### Day 2 Activities

**Focus of the day:** Finding Personal Symbolism  
**How will you know that students are getting it?** Finding Personal Symbolism, thumbnails for the final image
**How does the essential question connect students to this day’s focus?**

#### Process
**Warm Up:** I am Poem – Share out – Identify Personal Symbols in the poem.

**Individual/Pair Share:** Complete the Finding Personal Symbolism, Pair/Share with elbow partner to find out if the personal symbols can be understood by peers.

**Individual:** Log into p5.js - Create a canvas and load in pictures, draw basic shapes. 
Start to lay out the background/environment in p5.js

**Functions:**
- setup()
- draw()
- canvas methods and variables:
    * windowWidth()
    * windowHeight()
    background()
    frameRate()
- drawing methods:
    * rect()
    * ellipse()
    * fill()
    * stroke()
    * noStroke()

**Wrap Up:** Review the classes backgrounds, discus/determine next steps.  

### Day 3-5 Activities

**Focus of the day:** Studio Work

**How will you know that students are getting it?**
Engaged in the process. Walk through creating a portrait from observation.

#### Process
**Warm Up:** Image analysis.

**Individual:** Studio work period

**P5JS:** placing objects on the grid. Changing colors.
Full technical lesson plan created by Chelly Jin for Art+Code: [Instructional Art](https://processing.github.io/art-plus-code/instructionalArt-Intro/).

**Peer evaluation:** Use peer evaluation rubric and questions with at least one more work day to finish the image and mage changes.

**Wrap Up:** Personal connections in the portrait

### Day 5-7 Activities

**Focus of the day:** Incorporating technology, mixed media, and interactions into your collage.
**Essential Questions:**  How does incorporating mixed media, technology, and symbolism help tell more about you as an artist and your community through your work? 

#### Process
**Warm Up:** Image analysis
**Planning and prep:** students will look at the final portrait expectations and work on their proposal (see attached). Students will TPS their decisions and share out explaining their choices. 

**Technology:**
- p5.js Interactions
- mouseX
- mouseY
- Loop
- Saving pictures

Full technology resources view the lesson plan created by Chelly Jin for Art+Code here: [Interactive Art](https://processing.github.io/art-plus-code/interactiveArt-Intro/)

**Symbolism:** All students should have at least 3 symbols, they can be written, imagery, color ect… students should be able to explain their symbolism choices

**Mixed Media:** Students will use different media as an expression of symbolism and themselves.  They can draw shapes, load images, take photos, and lay them out in p5.js

### Final Day: Showcase

- Reflection
- Students interact with each others pieces
