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

# Introduction

# 2D Art

## Drawing & Painting
### [Precarious](https://camilleutterback.com/projects/precarious/) (2018)
Camille Utterback

![Camille Utterback, Precarious]({{ "https://camilleutterback.com/wp2022/wp-content/gallery/precarious-new/06.24.2019_Precarious_ScreenShot_001.jpg" | relative_url }})  
Close-up view of *Precarious*, interactive digital drawing.

> In the Precarious system, silhouettes are never fixed. As Utterback’s software draws peoples’ outlines, each line is translated into a series of points. The points are programmed to exert an animating force on the other points, which generates ongoing momentum in the continually redrawn forms. Each person’s silhouette is also visually altered by the movements of other people in the shared exhibition space. Past outlines are unintentionally erased as new participants enter the space and overwrite the previous projected imagery. Outlines are also intentionally refigured – as participants discover they can push and manipulate others’ existing outline marks with their own body. Pieces from one person’s silhouette move and accumulate onto another person’s outline, becoming shared evidence of both people’s presence in this space.
> 
> \- Camille Utterback

<iframe src="https://player.vimeo.com/video/344447606?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1013" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Precarious, 2018"></iframe>

### [*Possible, Plausible, Potential*](https://www.creativeapplications.net/project/possible-plausible-potential-drawings-of-architecture-generated-by-code/) (2015)
Made in [Processing](https://processing.org/) by Miguel Nóbrega

![Miguel Nóbrega, Possible, Plausible, Potential]({{ "/assets/images/curriculum/Unit-0_Sample-2.jpg" | relative_url }})  
Installation view of *Possible, Plausible, Potential*, pen plotter drawing.

> Nóbrega uses randomness as a way to partially abdicate control over the process. Randomness balances the authorship of the work between the artist and the code itself, or more specifically, the executable quality of code. Whatever emerges from executing the code cannot be entirely predicted from just reading it. Nóbrega understands his process as one of defining the boundaries in which experiments will take place. The outcomes of these experiments are sometimes unpredictable, which will most likely add up to the process in a feedback loop. The role of the artist ends up being to interpret the results and based on them to redefine the boundaries of the program.
>
> \- Filip Visnjic, Creative Applications

<iframe src="https://player.vimeo.com/video/143076578?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1080" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Superficie – Possible, plausible, potential"></iframe>

**Tips:** [p5.plotSvg](https://github.com/golanlevin/p5.plotSvg) is a tool that supports p5.js artists to download their sketches as SVG files, making it possible to connect p5.js with pen plotters. 
{: .notice--success}

## Printmaking
### [*Decode Kolams*](https://aarati.online/rituals-of-recursion) (2025)
Made in [p5.js](https://p5js.org) by Aarati Akkapeddi

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/cf3c70f922-1744573498/print_detail2.jpg" | relative_url }})  
Close-up view of *Decode Kolams*, screen-printed pattern generated in p5.js. 

> I developed a computer program that allows me to translate text into Kolam designs. Kolam (in Tamil) or Muggu (Telugu) is a traditional art form from South India. Kolams are auspicious drawings on the floor (usually at the threshold of the home) using rice flour. Kolams are traditionally made by women and created before sunrise. They comprise mathematically complex patterns that feature continuous intertwined lines.

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/c3185f1064-1744573494/diag.png" | relative_url }})  
*Decode Kolams* diagram, showing the correlation between visual pattern and binary code.

> To encode text into Kolam designs, I first translate each character into eight-digit binary codes (made from only 0s and 1s). I then use an algorithm to map this translation onto a diamond-shaped matrix of dots. The algorithm moves top to bottom and left to right, drawing loops on each dot that correspond with either 0 or 1 according to the binary code translation of the text. The algorithm connects these loops, making sure to never connect loops associated with “0” to those associated with “1”. The center of the matrix contains blank padding space, allowing the entire pattern to be distributed evenly on the matrix, preserving the perfect square/diamond shape.
>
> \- Aarati Akkapeddi

![Aarati Akkapeddi, Decode Kolams]({{ "https://aarati.online/media/pages/rituals-of-recursion/198e667c76-1744573500/prints.jpg" | relative_url }})  
Installation view at the Rituals of Recursion exhibition, Spill 180, NY.

**Tips:** You are invited to encode text into a kolam pattern using Aarati's software, [kolam.codes](https://kolam.codes/).
{: .notice--success}

## Photography
### [*Glance Back*](https://glanceback.info/) (2021)
Maya Man

> With this chrome extension, once a day at random when you open a new tab, Glance Back will quickly snap a photo of you and inquire: “What are you thinking about?”. Once you type your answer and press enter, the photo and thought will be collectively saved to your history of glances, cumulatively creating an archive of moments you share with your screen... When using our devices, we’re pulled into and solely focused on the glowing world that exists on the screen. We lose both an awareness of self and of the real world context surrounding us.
>
> \- Maya Man

![Maya Man, Glance Back]({{ "https://glanceback.info/assets/2022/question.png" | relative_url }})  
Software screenshot of *Glance Back*, a custom chrome extension software. 

> In every single photo Glance Back took, I was in the same room, wearing a near-identical sweatshirt, with a very similar expression on my face: intense concentration, with a tinge of agitation at my work being interrupted by the extension switching on. Each picture rankled me more than the previous day’s. Is that what I looked like? Why was I always scowling? Did I hate my job? Is that what my coworkers used to stare at every day in real life — a pinched, ferocious glower? 
>
> \-Mirel Zaman, REFINERY29

![Maya Man, Glance Back]({{ "https://glanceback.info/assets/2022/collection.png" | relative_url }})  
Maya Man's *Glance Back* archive. 

**Tips:** If you use the chrome browser, you can try Glance Back by installing the [chrome extension](https://chromewebstore.google.com/detail/glance-back/hgickafobcmcfffbjiamhhejkockfccm?pli=1).
{: .notice--success}

# 3D Art

## Sculpture
## Textile
### [Doilies](https://www.laurasplan.com/projects/doilies) (2004)
Laura Splan
![Laura Splan, Doilies]({{ "https://cdn.prod.website-files.com/6391e5efd5c2c1a8b351b8b8/64078a19a76aa391400a0de0_Laura_Splan%E2%80%942004%E2%80%94Doilies-SARS%E2%80%94computerized_machine_embroidered_lace.jpg" | relative_url }})  
Close-up view of *Dollies (SARS)*, computerized machine embroidered lace mounted on velvet.

> Doilies is a series of digitally fabricated lace sculptures depicting viruses created using a computerized embroidery process. The design of each doily in the series is based on a different enveloped virus structure (HIV, SARS, Influenza, Herpes, Hepadna). The radial symmetry of the doily and aesthetic conventions of lace are conflated with that of the virus structure. Here, the DNA, RNA, protein spikes, and lipid envelopes become unassuming decorative motif. The project explores the “domestication” of biomedical imagery in the quotidian landscape.
>
> \- Laura Splan 

![Laura Splan, Doilies]({{ "https://cdn.prod.website-files.com/6391e5efd5c2c1a8b351b8b8/640681a40983f6e9610d3f3f_Laura_Splan%E2%80%942009%E2%80%94commissioned_installation_for_Re-Formations_at_Van_Every-Smith_Galleries%E2%80%943.jpg" | relative_url }})  
Installation view at the Re/Formations exhibition, Van Every/Smith Galleries, NC

**Tips:** [PEmbroider](https://github.com/CreativeInquiry/PEmbroider) is an add-on tool that empowers Processing artists to export their sketches to a home embroidery machine!
{: .notice--success}


## Ceramic

### [*Lantern Vessel in Collage*](https://design-milk.com/f5-jolie-ngo-on-chicago-bricks-her-favorite-clogs-more/) (2024)
Jolie Ngo

> Ngo blends 3D-printing technology with hand-painted imagery influenced by the digital aesthetics of her childhood, as seen in Minecraft and The Sims. A Vietnamese-American creative, she also references her heritage. Faceted forms echo the look of traditional silk lanterns, while layered textures recall the topographic views of rice paddies.
>
> \- Anna Zappia, Design Milk 

![Jolie Ngo, installation]({{ "https://design-milk.com/images/2025/02/F5-Jolie-Ngo-Work-1-Lantern-Vessel-Collage.jpg" | relative_url }})  
Close-up view of *Lantern Vessel in Collage*, 3D-printed ceramic inspired by Vietnamese silk lanterns.

>I am deeply engaged in exploring the tension between past and future, probing the synergy between handmade arts and technology. Maintaining a sense of tactility, intimacy and sensitivity often achieved in traditional handworks is paramount to my practice. I lovingly dress these familiar forms with hand painted geometric patterns or hazy gradients and affix embellishments all over their surface to bring my hand back into the equation
>
> \- Jolie Ngo

![Jolie Ngo, installation]({{ "https://images.prismic.io/sayhito/5730abb2-712d-4314-83d9-449a82e425c1_sayhito_Jolie-Ngo_4.png?auto=compress,format" | relative_url }})  
Studio photography of Ngo's 3D-printed ceramic series. 

### [*Dust Furries*](https://www.unitedstatesartists.org/artists/linda-nguyen-lopez) (2019)
Linda Nguyen Lopez

![Linda Nguyen Lopez, Dust Furries]({{ "/assets/images/curriculum/Unit-0_Sample-3.png" | relative_url }})  
*Dust Furries*, a collection of 3D-printed ceramic.

> With verbal meaning so imprecise and mutable, visual language became my way of expressing the world. Clay, whose malleability allows me to create objects that appear soft and playful, has allowed for endless possibilities.
>
> \-Linda Nguyen Lopez

![Linda Nguyen Lopez, installation]({{ "https://artlogic-res.cloudinary.com/w_2400,c_limit,f_auto,fl_lossy,q_auto/ws-artlogicwebsite1040/usr/exhibitions/images/exhibitions/10/lopez-somebody-install7-web.jpg" | relative_url }})  
Installation view at the ʎpoqǝɯos exhibition, David B. Smith Gallery, CO

**Tips:** Developed by the [Machine Agency Lab](https://depts.washington.edu/machines/) at the University of Washington, [p5.fab](https://machineagency.github.io/p5.fab-docs/) brings p5.js and 3D printing together. 
{: .notice--success}

## Installation
## Architecture
## Public Art

# 4D Art

## Video & Animation

### The Earth Eaters (2025)
Made in [Processing](https://processing.org/) by Marina Zurkow and James Schmitz

![Marina Zurkow and James Schmitz, The Earth Eaters]({{ "/assets/images/curriculum/Unit-0_Sample-1.jpg" | relative_url }})  
Installation view at the Parting Worlds exhibition, Whitney Museum, NY.

> The Earth Eaters is an animated, software-based “fairy tale” that depicts an endless cycle of floating islands, animal inhabitants, and miners who hack away at the land. Together, these works evoke impermanence and loss as environments change and disappear due to human intervention and natural evolution.  
>
> \- Christiane Paul, Curator of Digital Art, Whitney Museum

<iframe src="https://player.vimeo.com/video/1074718891?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1080" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Marina Zurkow, &quot;The Earth Eaters&quot; (single channel), 2025"></iframe>

## Performance
### [Border Tuner / Sintonizador Fronterizo](https://www.lozano-hemmer.com/border_tuner__sintonizador_fronterizo.php) (2019)
Rafael Lozano-Hemmer
![Rafael Lozano-Hemmer, Border Tuner]({{ "/assets/images/curriculum/Unit-0_Sample-0.png" | relative_url }})  
Installation view at the Relational Architecture 23, Ciudad Juárez, México and El Paso, TX.
>Border Tuner is a large-scale, participatory art installation designed to interconnect the cities of El Paso, Texas, and Ciudad Juárez, Chihuahua. Powerful searchlights make “bridges of light” that open live sound channels for communication across the US-Mexico border. The piece creates a fluid canopy of light that can be modified by visitors to six interactive stations, three placed in El Paso and three in Juárez.
> 
> \- Rafael Lozano-Hemmer

<iframe width="560" height="315" src="https://www.youtube.com/embed/sX-VXlweApI?si=BhtyT-8vmbE7lPca&amp;start=180" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Dance
## Sound

