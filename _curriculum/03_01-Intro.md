---
# This is the frontmatter
title: "A Walk in the Neighborhood" # Title and Heading 1
permalink: /artTime-introduction/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: https://ids.si.edu/ids/deliveryService?id=SAAM-NJP.1.TV.42.1-.11_1&max=2600
    image_path: https://ids.si.edu/ids/deliveryService?id=SAAM-NJP.1.TV.42.1-.11_1&max=2600
    alt: "12 CRT televisions on pedestals displaying a single line at rotating angles"
    title: "Nam June Paik, TV Clock, 1963/1981, Smithsonian American Art Museum"
  - url: https://whitneymedia.org/assets/artwork/46048/T_2014_222_cropped.jpeg
    image_path: https://whitneymedia.org/assets/artwork/46048/T_2014_222_cropped.jpeg
    alt: "a black painting with white text reading JULY 4, 1967"
    title: "On Kawara, July 4, 1967, 1967, Whitney Museum"
---
![Create your own inspiration of time with p5.js.]({{ "/assets/images/curriculum/Unit-3_Sample-1.png" | relative_url }})

# Introduction

> I believe that if one takes a closer look at things, there is always a sort of sense of time involved. And I am very interested in how to make that visible. And this time that you take for looking at things, it also becomes a matter of space, of seeing space.
>
> \- Olafur Eliasson, 2014 lecture at the Massachusetts Institute of Technology

How do artists engage with the concept of time? This can include time-based media (a term describing art that unfolds over a span of time such as performance art, video, animation), illustrations of motion, or 2D drawings made over an accumulated time period. In this unit, we’ll use some of the p5.js tools that work with the computer’s clock and conditional statements to incorporate the element of time through animation into our digital drawings. 

The goal of this sequence is to have students create an original design for a clock, or find an interesting way of representing the passage of time. As some age groups and cohorts can find working with abstraction challenging, the visual ideas in this topic can be differentiated for the student group in two ways, pursuing abstraction and/or using text as a graphic element. Coding examples as well as artistic precedents for both directions are provided.


## Objectives
- Creating individual interpretations of "universal concepts"
- Working with automated elements in a composition
- **Visual Arts Vocabulary**: text, abstraction, movement


## Technical Terms & p5.js Elements
- [text()](https://p5js.org/reference/p5/text/) and text formatting functions
- escape sequences \n, \’, \”
- clock methods [hour()](https://p5js.org/reference/p5/hour/), [minute()](https://p5js.org/reference/p5/minute/), [second()](https://p5js.org/reference/p5/second/)
- arithmetic operators and expressions + - * /
- conditional statements if/else
- boolean expressions and operators >, <, >=, <=, ===, !==, &&, ||
- modulo operator %

  
## References & Artworks for Discussion: Interpretations of Time
{% include gallery%}
* Ho Tzu Nyen, [T for Time](https://www.singaporeartmuseum.sg/Art-Events/Exhibitions/Ho-Tzu-Nyen-Time-and-the-Tiger#artworks), 2023 - 
* Nam June Paik, [TV Clock](https://americanart.si.edu/artwork/tv-clock-80132), 1963/1981, Smithsonian American Art Museum
* Spencer Finch, [A Certain Slant of Light](https://www.spencerfinch.com/a-certain-slant-of-light), 2014, Morgan Library
* Yuko Mohri, [3 Musics](https://mohrizm.net/works/3-musics/), 2021
* Carlo Carrà, [Parole in Liberta](https://www.researchgate.net/figure/Parole-in-Liberta-Carlo-Carra-1914-Meggs-Purvis-2006-p-252_fig12_216473323), 1914
* Archie Moore, [kith and kin](https://www.kithandkin.me/documentation/panoramic), 2024, Venice Biennale Australia Pavilion
* Hiroshi Sugimoto, [Theatres](https://www.sugimotohiroshi.com/new-page-7), 1976 - 
* On Kawara, [July 4, 1967](https://whitney.org/collection/works/46048), 1967, Whitney Museum
* Christian Marclay, [The Clock](https://www.tate.org.uk/art/lists/five-ways-christian-marclays-clock-does-more-just-tell-time), 2010, Tate Modern


## Timeline
This project will take approximately four 45minute sessions:
1. Discussing artists, warm up activities, drafting a design, p5.js review
2. Working with text and clock variables
3. if/else statements, executing the clock design
4. Finalizing the clock design, sharing out


## Warm-Up Exercises
Some options for unplugged exercises:

### Mindfulness
- The goal of this activity is to share a meditative activity with students and also practice a little bit of mindfulness. Select at least 2 amounts of time including one ‘short’ and one ‘long’ such as 30 seconds and 10 minutes. Sit with students in silence for that duration of time, then discuss the physical experience of that time. 
- Some ways of facilitating that discussion include pair-sharing (small groups of students share with each other their experiences of that time and each group shares out a summary) and creating a word cloud of the board of key words students would use to describe their experience (“long”, “short”, “surprising”)
- The goal of the exercise is for the students to have some concrete descriptors to draw from and reference as they create their designs. Helpful questions for students to discuss might be “What kind of physical sensations did you feel in your body, such as twitchiness or calm”, “What did you focus your eyesight on during this unit of time?”, “What are some things you noticed in the room that you might not have noticed before?” and “What emotions might you connect with these units of time?”

### Times of Day
- Have students write or sketch an object or location at different times of day, from morning, mid-afternoon, to evening such as a plant or room. 
- Consider the intensity and color of light, surrounding objects, any possible movements.

### Long exposure photography
- If a dark environment and photographic equipment (cameras, tripods) are available, students can try out long exposure photography to gain a sensitivity for light-based information accumulating on a surface.
- In pairs or groups of three, students set up cameras (or smart devices with manual camera apps installed) with tripods. The cameras should have long shutter speeds, ranging from 1 second to manually open to create long exposure photographs. 
- Incorporating lights, either with small LEDs or the flash of their phone can allow for students to create light paintings.

- Drafting an Original Clock Design
  - To prepare for the project  of designing a clock, students draft a design for an original clock. Depending on the age group and differentiation needs of the students, useful guidelines or constraints might be “no numbers”, “only use the shapes we’ve tried so far in p5.js”
  - Have students create a design for a clock using paper cutouts of shapes (á la Matisse) or letters (in the style of Italian Parole in Liberta). 
