---
# This is the frontmatter
title: "Lost and Found" # Title and Heading 1
permalink: /lostAndFound-intro/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: https://artuk.org/learn/learning-resources/the-superpower-of-looking-yayoi-kusamas-spotty-pumpkin
    image_path: https://d3d00swyhr67nd.cloudfront.net/w800h800/artuk/yayoi-kusama-pumpkin-2018-1.jpg
    alt: "black and white abstract drawing of curves with handwritten text: too much future "
    title: "Pumpkin, 2018, Yayoi Kusama"
  - url: https://www.youtube.com/watch?v=nrKIGL5ZWNk
    image_path: https://www.themodern.org/sites/default/files/2019-07/Walker_Slavery%21-Slavery%21_1.jpg
    alt: "abstract drawings of straight and curved lines of varying thickness"
    title: "Exploring Kara Walker’s Radical Use of Silhouettes, Art21"
  - url: https://www.xubing.com/en/work/details/188?classID=1&type=class#188
    image_path: https://gwarlingo.com/wp-content/uploads/2021/04/Xu-Bing-06-1.jpg
    alt: "sketched portrait of a young man"
    title: "Book from the Ground, Xu Bing"
---

Lost and Found remixes Critical Computation by Xin Xin and Katherine Moriwaki, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en).

![Create a digital drawing tool with p5.js!]({{ "/assets/images/curriculum/Unit-1_Sample-6.png" | relative_url }})  
[The Necklace](https://cc-lab-portfolio-ardak.glitch.me/p1.html). Made in [p5.js](https://p5js.org/) by Ardak Mukanova.

# Introduction

We remember the past through words and images. When we describe a memory to a friend, our spoken words construct an image in their mind. This image is their interpretation of our memory and, most likely, will look very different from the actual image in our mind.

If I ask you to describe your friend’s face to me, you might say, “brown hair, brown eyes, freckles,” but that description applies to many people, and might not help me identify your friend when I run into them next time. Humans can communicate imperfectly and still convey meaning because we expect and accept some level of ambiguity. In contrast, when we communicate with a computer through code, we must be very precise because it doesn’t interpret or infer the way a human does.

For example, this is how a smiley face is described in human language (what we might say) versus computer language (code):

<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr style="background-color: black; color: white;">
      <th style="padding: 8px; text-align: left;">Human Language</th>
      <th style="padding: 8px; text-align: left;">Computer Language</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px;">The person is looking straight ahead</td>
      <td style="padding: 8px;"><code>noFill();</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;">and carrying a smile.</td>
      <td style="padding: 8px;"><code>strokeWeight(4);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>stroke(0);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>ellipse(200, 200, 100, 100);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>arc(200, 215, 33, 30, 0, PI);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>fill(0);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>ellipse(180, 190, 10, 10);</code></td>
    </tr>
    <tr>
      <td style="padding: 8px;"></td>
      <td style="padding: 8px;"><code>ellipse(220, 190, 10, 10);</code></td>
    </tr>
  </tbody>
</table>

This topic explores the ambiguity in human language and the gap between how humans and computers understand it. Even with the advancement of computer-generated imagery, like OpenAI’s ChatGPT, DALL-E, and even AI-generated TikTok filters, the same text prompt will still generate a wide variety of different results, revealing the differences between human intention and machine interpretation.

Completed in pairs of two, you will work with a partner and exchange detailed descriptions of a personal object you have lost in the past. Then, based on the descriptions, you will re-create the object for your partner using computer code with p5.js.

## Premise

Draw an object described to you in plain language through code.

## Learning Objectives

### Grade 6~8

- Foundational understanding of the p5.js Editor environment and basic drawing features.
- Gaining insights into assembling complex shapes using primitive shapes only.
- Comprehending visual arts vocabularies, including shape, size, color, composition, symmetry, and asymmetry.
- Comparing tradeoffs between allowing information to be public and keeping information private and secure.
- Ability to explain potential security threats and security measures to mitigate threats.

### Grade 9~12

- Comprehending and translating between different representations of data abstractions in color.
- Gaining insights into transformation features in p5.js.

## Technical Terms & p5.js Elements

### Grade 6~8

- [setup()](https://p5js.org/reference/p5/setup/), [draw()](https://p5js.org/reference/p5/draw/)
- Cartesian coordinate system
- [rect()](https://p5js.org/reference/p5/rect/), [ellipse()](https://p5js.org/reference/p5/ellipse/)
- Anchor point
- [rectMode()](https://beta.p5js.org/reference/p5/rectmode/), [ellipseMode()](https://beta.p5js.org/reference/p5/ellipsemode/)
- [fill()](https://p5js.org/reference/p5/fill/)
- [stroke()](https://p5js.org/reference/p5/stroke/), [noStroke()](https://p5js.org/reference/p5/noStroke/)
- Arithmetic operators: +, -

### Grade 9~12

- [colorMode()](https://beta.p5js.org/reference/p5/colormode/)
- [blendMode()](https://beta.p5js.org/reference/p5/blendmode/)
- [scale()](https://beta.p5js.org/reference/p5/scale/), [translate()](https://beta.p5js.org/reference/p5/translate/), [push()](https://beta.p5js.org/reference/p5/push/), [pop()](https://beta.p5js.org/reference/p5/pop/)

## References & Artworks for Discussion

{% include gallery%}

- [Pumpkin, 2018](https://artuk.org/learn/learning-resources/the-superpower-of-looking-yayoi-kusamas-spotty-pumpkin), Yayoi Kusama
- [Exploring Kara Walker’s Radical Use of Silhouettes](https://www.youtube.com/watch?v=nrKIGL5ZWNk), Art21
- [Book from the Ground](https://www.xubing.com/en/work/details/188?classID=1&type=class#188), Xu Bing

## Timeline

This project will take approximately three to four 45-minute sessions:

1. Discussing art references, warm-up Exercise, introduction to p5.js.
1. Assigning partners. Exchanging detailed descriptions of lost objects.
1. Recreating the partner’s lost object using p5.js.
1. Sharing out.

## Warm-Up Exercise

### Planning your Lost & Found Project

1. Students exchange written descriptions of their objects with one another.
1. Then, each partner draw the object on paper by using ellipses and rectangles only.
1. After 5 minutes of drawing, students take turns showing their drawing to the other for feedback. Feedback should be minimal and should not add too many complicated elements to the original drawing.
