---
# This is the frontmatter
title: "Responsive Visual Data" # Title and Heading 1
permalink: /responsivevisualdata-intro/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: /assets/images/thumbnails/unit4.png
    image_path: /assets/images/thumbnails/unit4.png
    alt: "Screenshot of a digital mask using the p5.js web editor"
    title: "Sound Reactive Mask"

---

![Create a sound-reactive mask with p5.js!]({{ "/assets/images/unit4.png" | relative_url }})  

# Introduction & Inspiration

*How can art transform our relationship to data and information? How can we leverage computation’s ability to cull, sort, and interact with data to produce meaningful or exciting artwork? How might data and its uses engage the audience more deeply?* 

A fundamental concept in code is the input and the output — taking data in, and creating, refining, remapping something from it. Data, in this sense, is broader than the simple spreadsheet of numbers; but rather, the concept of how information is circulated throughout a system for optimization or curation. Data has become ubiquitous and far-reaching; from the ways that bits and bytes are physically stored to its persistence in organizing information. However, we can use this concept of data structure to look at how modern and contemporary artists are using all kinds of data and information to create meaningful artwork to reflect, resist and understand the current condition.

In this topic, we’ll use p5.js to create a sound-reactive art project, using variables to understand the way data can feed into various inputs and output.

***Related spheres: Data Visualization, Infographic Design, Immersive Data Installations***


## Objectives

- Understanding the basics of variables (storing, containing or passing data), inputs, and outputs
- Becoming comfortable with creating variables, integrating arithmetic, as well as using new functions (ie. map() or constrain() )
- Creating a sound-reactive illustration or face mask that interacts to a mic input’s volume
- Learning about how artists use data in their practice, how variables works a metaphor for data art, and various data artists


## References & Artworks for Discussion

Mimi Onuoha, [The Library of Missing Datasets](https://mimionuoha.com/the-library-of-missing-datasets)

Mimi Onuoha, [Machine Sees More Than it Says](https://mimionuoha.com/machine-sees-more-than-it-says)

Golan Levin, [Re:FACE](https://www.flong.com/archive/projects/reface-anchorage/index.html)

Refik Anadol, [Archive Dreaming - AI Data Sculpture](https://refikanadol.com/works/archive-dreaming/) 

Aaron Koblin, [Flight Patterns](https://www.aaronkoblin.com/project/flight-patterns/) 

Romi Morrison, [Decoding Possibilities](https://elegantcollisions.com/decoding-possibilities) 

Romi Morrison, [The Future Conditional](https://elegantcollisions.com/the-future-conditional) 

## Related Artists Discussion Questions

1. In what ways do these artists challenge traditional notions of computation and coding? Conversely, how might they challenge traditional notions of art?
2. Some of the artists are utilizing art as a visualization technique for the data they’re wishing to delve deeper in; whereas some artists are utilizing art as a means to disrupt or remix the data from its initial origins to reproduce new meaning. What are some ways you’ve seen artists or communities take information and data to help bridge various understandings, reconnect to histories that were suppressed, or highlight archives that might be lost to the sands of time? 
3. Romi Morrison’s work takes physical manifestations of data (archived prints, archival material, and primary sources) and revisits them in a curation that allows for deeper conversation. How does this change or illicit new understandings of data in art? 
4. Mimi Onuoha curates a series of datasets that are missing as a new form of a dataset. How can datasets offer narrative, shape representation, or reveal biases? 



# Unplugged Activities
## Programmatic Drawing

Let’s create a series of drawings on paper to explore some of the fundamentals of thinking in systems and writing code. We’ll explore grid structures, chance operations, binary trees, collaborative drawing, and other topics.

### MESH

1. Draw a triangle
2. Use one edge of the triangle and two new lines to draw a new triangle, but don’t intersect with another triangle
3. Repeat 2, until the drawing is finished

### BINARY

1. Draw a line from the edge of the drawing area toward the center
2. Draw two lines growing from the open endpoint of the line
3. For each new line drawn in 2, repeat 2

### NETWORK

### (PHASE 1)

A. Draw a dot on the paper

B. Draw another dot in the most empty space on the page

C. Take turns; repeat B until satisfied with the density

### (PHASE 2)

A. Draw a circle around the first dot

B. Draw a circle around the closest dot and make sure the circle overlaps the last drawn circle

C. Take turns; repeat B until each dot has a circle

### (PHASE 3)

A. Take turns drawing a strong, straight line to connect the center points of each overlapping circle
