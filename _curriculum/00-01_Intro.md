---
# This is the frontmatter
title: "Code as Creative Medium" # Title and Heading 1
permalink: /codeAsCreativeMedium-intro/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
  - url: https://www.lozano-hemmer.com/border_tuner__sintonizador_fronterizo.php
    image_path: "/assets/images/curriculum/Unit-0_Sample-0.png"
    alt: "black and white abstract drawing of curves with handwritten text: too much future "
    title: "Rafael Lozano-Hemmer, Border Tuner / Sintonizador Fronterizo, Relational Architecture 23, 2019."
  - url: https://www.youtube.com/watch?v=nrKIGL5ZWNk
    image_path: https://www.themodern.org/sites/default/files/2019-07/Walker_Slavery%21-Slavery%21_1.jpg
    alt: "abstract drawings of straight and curved lines of varying thickness"
    title: "Exploring Kara Walker’s Radical Use of Silhouettes, Art21"
  - url: https://www.xubing.com/en/work/details/188?classID=1&type=class#188
    image_path: https://gwarlingo.com/wp-content/uploads/2021/04/Xu-Bing-06-1.jpg
    alt: "sketched portrait of a young man"
    title: "Book from the Ground, Xu Bing"
---

# What is Creative Coding?

Computer code is a set of directions we give a computer to carry out commands. When working on a website, a computer programmer tells the computer where to put a button and what that button should do when we click on it. What we code doesn’t only have to be functional; it can make us feel, think, and connect. We can make art with code. 
Coding is a powerful tool for artistic expression because it is dynamic. If you want the colors on the screen to change when the user clicks a button or if you want an animated scene, code can help you bring those ideas to life. 

Code lets artists:
- Draw pictures that move and change
- Make interactive art that responds to human action
- Create sculptures using 3D printers
- Build experiences that tell stories

## 2D Art

### Drawing & Painting
#### [*Precarious*](https://camilleutterback.com/projects/precarious/) (2018)
Camille Utterback

![Camille Utterback, Precarious]({{ "https://camilleutterback.com/wp2022/wp-content/gallery/precarious-new/06.24.2019_Precarious_ScreenShot_001.jpg" | relative_url }})  
Close-up view of *Precarious*, interactive digital drawing.

In this art piece, the programmer uses cameras to detect human movement. The program draws an outline around that movement, and then makes those outlines interact with other people’s outlines as a series of dots. These dots connect and dance with other people's dots, creating a constantly changing picture.

<iframe src="https://player.vimeo.com/video/344447606?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1013" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Precarious, 2018"></iframe>

##### Think About
- How does the computer "see" people moving?
- What makes this artwork different from a regular painting?


#### [*Possible, Plausible, Potential*](https://www.creativeapplications.net/project/possible-plausible-potential-drawings-of-architecture-generated-by-code/) (2015)
Made in [Processing](https://processing.org/) by Miguel Nóbrega

![Miguel Nóbrega, Possible, Plausible, Potential]({{ "/assets/images/curriculum/Unit-0_Sample-2.jpg" | relative_url }})  
Installation view of *Possible, Plausible, Potential*, pen plotter drawing.

This artist wrote code that draws pictures, but he let the computer make some choices on its own. He told the computer the basic rules (like "stay inside these lines"), but let it decide where to draw each line, making each piece more of a “conversation” between the artist and the computer.

> Nóbrega understands his process as one of defining the boundaries in which experiments will take place. The outcomes of these experiments are sometimes unpredictable, which will most likely add up to the process in a feedback loop. The role of the artist ends up being to interpret the results and based on them to redefine the boundaries of the program.
>
> \- Filip Visnjic, Creative Applications

<iframe src="https://player.vimeo.com/video/143076578?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1080" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Superficie – Possible, plausible, potential"></iframe>

##### Think About
- How does Nóbrega use code to create a balance between randomness and structure?
- What creative decisions are made through writing code, and what are left to the machine?
- In what ways does code become an artistic collaborator in this work?

**Tip:** [p5.plotSvg](https://github.com/golanlevin/p5.plotSvg) is a tool that supports p5.js artists to download their sketches as SVG files, making it possible to connect p5.js with pen plotters. 
{: .notice--success}

### Printmaking
#### [*Decode Kolams*](https://aarati.online/rituals-of-recursion) (2025)
Made in [p5.js](https://p5js.org) by Aarati Akkapeddi

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/cf3c70f922-1744573498/print_detail2.jpg" | relative_url }})  
Close-up view of *Decode Kolams*, screen-printed pattern generated in p5.js. 

Kolams are beautiful patterns that women in South India have drawn for hundreds of years. 

> Kolams are traditionally made by women and created before sunrise. They comprise mathematically complex patterns that feature continuous intertwined lines.
>
> \- Aarati Akkapeddi

By converting characters into binary code and mapping them onto a grid, Akkapeddi’s algorithm makes intricate patterns that honor the mathematical complexity of Kolams. The combination of language, code, and cultural expression prompts us to consider how cultural heritage and technology intersect.

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/c3185f1064-1744573494/diag.png" | relative_url }})  
*Decode Kolams* diagram, showing the correlation between visual pattern and binary code.

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/198e667c76-1744573500/prints.jpg" | relative_url }})  
Installation view at the Rituals of Recursion exhibition, Spill 180, NY.

##### Think About
- How is code used to translate texts into visual form?
- How can technology help keep old traditions alive?
- Can you think of other ways to represent code?

**Tip:** You are invited to encode text into a kolam pattern using Akkapeddi's software, [kolam.codes](https://kolam.codes/).
{: .notice--success}

### Photography
#### [*Glance Back*](https://glanceback.info/) (2021)
Maya Man

Have you ever wondered what you look like when you're focused on your computer? This artist made a program that randomly takes a photo of you while you're browsing the internet. It also asks what you're thinking about. Over time, you build a collection of these surprise photos and thoughts.

> With this chrome extension, once a day at random when you open a new tab, Glance Back will quickly snap a photo of you and inquire: “What are you thinking about?”. Once you type your answer and press enter, the photo and thought will be collectively saved to your history of glances, cumulatively creating an archive of moments you share with your screen. 

![Maya Man, Glance Back]({{ "https://glanceback.info/assets/2022/question.png" | relative_url }})  
Software screenshot of *Glance Back*, a custom chrome extension software. 

> When using our devices, we’re pulled into and solely focused on the glowing world that exists on the screen. We lose both an awareness of self and of the real world context surrounding us.
>
> \- Maya Man

![Maya Man, Glance Back]({{ "https://glanceback.info/assets/2022/collection.png" | relative_url }})  
Maya Man's *Glance Back* archive. 

##### Discussion Prompts
- How does the use of code shape the interaction between the viewer and the artwork in this piece?
- What does this work tell us about how code can collect, curate, and reframe everyday behavior?
- How does this creative use of code shape our understanding of who is in control in digital spaces?

**Tip:** If you use the chrome browser, you can try Glance Back by installing the [chrome extension](https://chromewebstore.google.com/detail/glance-back/hgickafobcmcfffbjiamhhejkockfccm?pli=1).
{: .notice--success}

## 3D Art

### Sculpture
#### [*She Who Sees the Unknown*](https://shewhoseestheunknown.com/) (2017-2021)
Morehshin Allahyari (Persian: موره شین اللهیاری‎)

![Morehshin Allahyari, She Who Sees the Unknown]({{ "https://i0.wp.com/shewhoseestheunknown.com/wp-content/uploads/2020/03/AllahyariM-SWSTU-TheLaughingSnake-01-5428x7286-1-scaled.jpg?ssl=1" | relative_url }})  
Close-up view of *The Laughing Snake (Persian: مار قهقهه)*, a 3D-printed figure.

This artist uses 3D modeling software (like digital clay) to recreate mythical creatures from Middle Eastern stories. Many of these stories were lost or forgotten over time. By rebuilding these creatures with code and 3D printing them, she brings old stories back to life.

![Morehshin Allahyari, She Who Sees the Unknown]({{ "https://i0.wp.com/shewhoseestheunknown.com/wp-content/uploads/2019/03/morehshin_allahyari-she_who_sees_the_unknown-transfer_gallery-19.jpg?ssl=1" | relative_url }})  
Installation view at the She Who Sees the Unknown exhibition, Transfer Gallery, NY

> My work undermines the uneven economics of Western technocolonialism and the performative rhetoric of Islamic fundamentalism, through a ficto-feminist-figural expression of power.
>
> \- Morehshin Allahyari

##### Think About
- How can 3D printing help save stories from the past?
- What stories from your culture could be brought back with technology?
- How is making 3D art with code different from carving with your hands?

### Textile
#### [*Doilies*](https://www.laurasplan.com/projects/doilies) (2004)
Laura Splan
![Laura Splan, Doilies]({{ "https://cdn.prod.website-files.com/6391e5efd5c2c1a8b351b8b8/64078a19a76aa391400a0de0_Laura_Splan%E2%80%942004%E2%80%94Doilies-SARS%E2%80%94computerized_machine_embroidered_lace.jpg" | relative_url }})  
Close-up view of *Dollies (SARS)*, computerized machine embroidered lace mounted on velvet.

Have you ever seen those fancy lace decorations someone might put under their teacup during tea time? Those are called doilies. This artist used code to design doily patterns, but instead of flowers, her patterns are based on the shapes of viruses! She then used special machines to embroider these organic-looking doilies.

![Laura Splan, Doilies]({{ "https://cdn.prod.website-files.com/6391e5efd5c2c1a8b351b8b8/640681a40983f6e9610d3f3f_Laura_Splan%E2%80%942009%E2%80%94commissioned_installation_for_Re-Formations_at_Van_Every-Smith_Galleries%E2%80%943.jpg" | relative_url }})  
Installation view at the Re/Formations exhibition, Van Every/Smith Galleries, NC

##### Think About
- How does using a computer change traditional crafts like embroidery?
- How does using code to generate visual patterns change the meaning of an art form or craft conventionally designed by hand?
- How can code help us see everyday things in new ways?

**Tip:** [PEmbroider](https://github.com/CreativeInquiry/PEmbroider) is an add-on tool that empowers Processing artists to export their sketches to a home embroidery machine!
{: .notice--success}

### Ceramic
#### [*Lantern Vessel in Collage*](https://design-milk.com/f5-jolie-ngo-on-chicago-bricks-her-favorite-clogs-more/) (2024)
Jolie Ngo

![Jolie Ngo, installation]({{ "https://design-milk.com/images/2025/02/F5-Jolie-Ngo-Work-1-Lantern-Vessel-Collage.jpg" | relative_url }})  
Close-up view of *Lantern Vessel in Collage*, 3D-printed ceramic inspired by Vietnamese silk lanterns.

> Ngo blends 3D-printing technology with hand-painted imagery influenced by the digital aesthetics of her childhood, as seen in Minecraft and The Sims. A Vietnamese-American creative, she also references her heritage. Faceted forms echo the look of traditional silk lanterns, while layered textures recall the topographic views of rice paddies.
>
> \- Anna Zappia, Design Milk 

![Jolie Ngo, installation]({{ "https://images.prismic.io/sayhito/5730abb2-712d-4314-83d9-449a82e425c1_sayhito_Jolie-Ngo_4.png?auto=compress,format" | relative_url }})  
Studio photography of Ngo's 3D-printed ceramic series. 

##### Think About
- How can you tell which parts were made by a computer and which by hand?
- What opportunities does generative design through code offer to ceramic or physical practices?
- How does code expand the definition of craft?


#### [*Dust Furries*](https://www.unitedstatesartists.org/artists/linda-nguyen-lopez) (2019)
Linda Nguyen Lopez

![Linda Nguyen Lopez, Dust Furries]({{ "/assets/images/curriculum/Unit-0_Sample-3.png" | relative_url }})  
*Dust Furries*, a collection of 3D-printed ceramic.

*Dust Furries* are ceramic sculptures inspired by computational simulations of particle systems. These forms, reminiscent of dust bunnies or organic growths, navigate the intersection of randomness and structure, showcasing how code can inform and inspire physical artistry.

> With verbal meaning so imprecise and mutable, visual language became my way of expressing the world. Clay, whose malleability allows me to create objects that appear soft and playful, has allowed for endless possibilities.
>
> \-Linda Nguyen Lopez

![Linda Nguyen Lopez, installation]({{ "https://artlogic-res.cloudinary.com/w_2400,c_limit,f_auto,fl_lossy,q_auto/ws-artlogicwebsite1040/usr/exhibitions/images/exhibitions/10/lopez-somebody-install7-web.jpg" | relative_url }})  
Installation view at the ʎpoqǝɯos exhibition, David B. Smith Gallery, CO

##### Discussion Prompts

- What adjectives might you use to describe Lopez's visual language?
- How might this work shift our understanding of what kinds of forms or textures code can generate?
- How does the artist balance algorithmic design with gravity and weight of the physical form?

**Tip:** Developed by the [Machine Agency Lab](https://depts.washington.edu/machines/) at the University of Washington, [p5.fab](https://machineagency.github.io/p5.fab-docs/) brings p5.js and 3D printing together. 
{: .notice--success}

<!-- ## Installation
## Architecture
## Public Art -->

## 4D Art
### Video & Animation
#### *The Earth Eaters* (2025)
Made in [Processing](https://processing.org/) by Marina Zurkow and James Schmitz

![Marina Zurkow and James Schmitz, The Earth Eaters]({{ "/assets/images/curriculum/Unit-0_Sample-1.jpg" | relative_url }})  
Installation view at the Parting Worlds exhibition, Whitney Museum, NY.

Using code, these artists created an endless animation that tells a story about floating islands. Little creatures live on the islands, but miners keep digging away the land. The story never stops - it keeps cycling through creation and destruction.

<iframe src="https://player.vimeo.com/video/1074718891?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1080" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Marina Zurkow, &quot;The Earth Eaters&quot; (single channel), 2025"></iframe>

##### Think About
- How can code help tell stories that never end?
- What emotions do you feel watching things being built and destroyed?
- How is this artwork different from a regular movie?

### Interactive Performance
#### [*Border Tuner / Sintonizador Fronterizo*](https://www.lozano-hemmer.com/border_tuner__sintonizador_fronterizo.php) (2019)
Rafael Lozano-Hemmer

![Rafael Lozano-Hemmer, Border Tuner]({{ "/assets/images/curriculum/Unit-0_Sample-0.png" | relative_url }})  
Installation view at the Relational Architecture 23, Ciudad Juárez, México and El Paso, TX.

This artwork connects people in Mexico and the United States using light and sound. When someone speaks on one side of the border, a bright search light projects to the other side of the border. People can have conversations across the border using this special technology.

<iframe width="560" height="315" src="https://www.youtube.com/embed/sX-VXlweApI?si=BhtyT-8vmbE7lPca&amp;start=180" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

##### Think About

- How are human inputs sensed, interpreted, and responded to in this piece?
- How can technology bring people together instead of keeping them apart?
- How can creative coding shift the function of technology from controlling us to connecting us and encouraging communication?

## Why Use Code to Make Art?
Code is special because it can:
- Respond to people - Art can change based on how you move or what you do
- Never stop changing - Digital art can keep evolving and growing
- Combine old and new - Artists can mix traditional techniques with computer power
- Tell interactive stories - You can be part of the artwork, not just look at it
- Preserve culture - Old traditions can be saved and shared in new ways

<!-- ## Dance
## Sound -->

