---
title: "Units"
permalink: /introduction/

# Include links, images, and descriptions for each unit row below:
unit1_row: # One row that has two columns (1 column for each unit)
  - image_path: /assets/images/curriculum/Unit-1_Sample-0.png # Add image in /assets/images and link it here
    title: "Lost and Found" # Include a title
    excerpt: | # Multi-line description
        *Design a digital drawing tool using p5.js. Customize your tool to express unique qualities of line and composition!* 
        - p5.js setup & structure
        - drawing methods
        - mouse and key inputs
    url: /lostAndFound-intro/ # Include the permalink specified on the unit's page

  - image_path: /assets/images/curriculum/Unit-2_Sample-0.png
    title: "Mask Generator"
    excerpt: |
        *Use shapes, images, text and color to create an "About Me" collage to create a self-portrait while exploring the p5.js editor and its many features.* 
        - p5.js Editor
        - drawing methods
        - text methods
        - loading and displaying images
    url: /collaginginstructions-intro/

unit2_row:
  - image_path: /assets/images/curriculum/Unit-3_Sample-4.png
    title: "A Walk in the Neighborhood"
    excerpt: |
        *Bring together drawing, animation and the computer's clock to engage with **time** as an artistic concept and design your own clock!*
        - working with text in p5.js
        - clock methods
        - arithmetic operators and expressions
        - if/else statements
        - boolean expressions and operators
    url: /artTime-introduction/

  - image_path: /assets/images/curriculum/Unit-4_Sample-0.png
    title: "Drawing Machine"
    excerpt: |
        *Use variables to create a sound-reactive art project and understand the way data can feed into inputs and outputs*
        - variables
        - map(), constrain() functions
        - p5.js Sound Library
    url: /responsivevisualdata-intro/

unit3_row:
  - image_path: /assets/images/curriculum/Unit-5_Sample-0.png
    title: "Movement, Collaboration & Harmony"
    excerpt: |
        *Collaborate with code to create animated drawings that add up to more than the sum of their parts.*
        - animation
        - variable declaration & instantiation
        - functions & parameters
    url: /movementCollaborationHarmony-intro/

  - image_path: /assets/images/curriculum/Unit-6_Sample-0.png
    title: "Creating with Interactivity"
    excerpt: |
        *Consider interactivity while creating a drawing tool that responds to user inputs.*
        - conditional statements and computational logic
        - mouse and key functions
        - booleans and operators
    url: /creatinginteractivity-intro/

unit4_row:
  - image_path: /assets/images/curriculum/Unit-7_Sample-5.png
    title: "Observing Patterns"
    excerpt: |
        *Recreate patterns from daily life to practice close observation and iteration.*
        - for loops
        - random methods
        - nested for loops
    url: /patterns-intro/

  - image_path: /assets/images/curriculum/Unit-8_Sample-0.png
    title: "Generative Patterns & Weaving"
    excerpt: |
        *Create a “weaving” program that generates new, unique patterns based on programmatic randomness.*
        - random() methods and randomness
        - frame rate and p5.js looping mechanism
        - for loops
        - nested for loops
        - while, do loops
    url: /generativeweaving-intro/

---

The Art + Code’s curriculum is a visual arts forward approach that drives an understanding of core programming concepts through an art-focused lens. Designed for K-12 Educators, this curriculum explore a range of technical and artistic topics grouped into four categories: Start Here!, Bringing Numbers to Life, Creative Coding, and Generating Patterns. 

Each module provides resources to support student artistic development including 'unplugged' warm-up activities, tips for teaching code, discussion prompts and suggestions for assessment activities. Each unit provides a glimpse into an artistic practice supported by code, or digital media driven by visual arts ideas. 

The modules here are designed to meet teachers and students where they’re at: first time coders, interactive media art enthusiasts and artists looking for new tools to incorporate into their practice.

For additional curricular resources designed by the Art+Code participants, visit the [Resources page]({{ site.baseurl }}{% link _pages/resources.md %}).

## Start Here!

{% include curriculum_feature_row.html id="unit1_row" %}

## Bringing Numbers to Life

{% include curriculum_feature_row.html id="unit2_row" %}

## Creative Coding

{% include curriculum_feature_row.html id="unit3_row" %}

## Generating Patterns

{% include curriculum_feature_row.html id="unit4_row" %}
