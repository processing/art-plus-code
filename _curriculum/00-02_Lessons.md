---
# This is the frontmatter
title: "Code as Creative Medium" # Title and Heading 1
permalink: /codeAsCreativeMedium-lessons/ # Give your page a permalink
published: true

gallery: # Below is for including an image gallery
---
# Lesson Plans & Technical Steps

## 1. Setting Up Your Environment

To begin writing code using [p5.js](https://p5js.org/), you need to set up the coding environment to write and save your programs. [Processing Foundation](https://processingfoundation.org/) provides the [p5.js Editor](https://editor.p5js.org/), a website where programmers can write, test, share, and remix p5.js programs without needing to download or install a code editor on a computer. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/MXs1cOlidWs?si=h8uilatDVzeLCl_a" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### What you will need
- Access to the internet and the latest version of a desktop browser such as:
  - Chrome (recommended)
  - Firefox (recommended)
  - Safari
  - Edge
- A desktop computer, laptop, or Chromebook

### 1A. Opening the p5.js Editor
1. Open the latest version of Chrome or Firefox browser on your computer and visit the [p5.js Editor](https://editor.p5js.org/) website. 
1. Click the “Sign up” link on the top right of the web page.

![p5.js Editor sign-up link]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_sign_up.png?raw=true" | relative_url }})  

### 1B. Creating an Account
Create an account on the [p5.js Editor](https://editor.p5js.org/) using one of the following options:
- Manual sign-up
  - Create a username.
  - Enter your email address.
  - Create and confirm a password. 
  - Click the “Sign Up” button.

![p5.js Editor sign-up page]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_sign_up_page.png?raw=true" | relative_url }}) 

- Using a Google account
  - Click the button at the bottom of the page labeled “Login with Google.” 
  - Follow the prompts to enter your email and password for your Google account. 

- Using a GitHub account
  - Click the button at the bottom of the page labeled “Login with GitHub.” 
  - Follow the prompts to enter your username and password for GitHub.
  - Authorize the [p5.js Editor](https://editor.p5js.org/) to access your GitHub details by clicking the “Authorize processing” button.

### 1C. Exploring the p5.js Editor and running your first “sketch”

  ![p5.js Editor interface breakdown]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_interface_breakdown.png?raw=true" | relative_url }}) 

1. Now that you’ve created an account, which allows you to save and share your work, we’re ready to take a deeper look at [p5.js Editor](https://editor.p5js.org/)’s interface.
1. You have the option of switching to another language by clicking on "English" in the navigation menu. 
1. You also have the option to make the interface more accessible by clicking on Settings in the toolbar and updating Theme, Text Size, and Accessibility for screen readers. 
1. To view the output of the default code inside the text editor, click the Play button in the top left corner.    ![p5.js Editor interface breakdown]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_running_a_sketch.png?raw=true" | relative_url }}) 
1. After clicking the Play button, you can expect to see a light gray canvas, measuring 400 x 400 pixels, appear in the preview area. We invite you to update one of the “400” numbers inside the text editor to a smaller number, click on the Play button again, and see what happens! 😃
1. Last but not least, the [p5.js Editor](https://editor.p5js.org/) defaults to using [p5.js](https://p5js.org/) version 1.11.5. However, we will be covering some exciting and new p5.js features in this lesson plan, so please change your settings to switch over to the latest version of p5.js.
![p5.js Editor version switcher]({{ "/assets/images/ui/version_switcher_1.png" | relative_url }}) 
![p5.js Editor version switcher]({{ "/assets/images/ui/version_switcher_2.png" | relative_url }}) 
![p5.js Editor version switcher]({{ "/assets/images/ui/version_switcher_3.png" | relative_url }}) 

### 1D. Renaming, saving, and sharing sketches
1. By default, the [p5.js Editor](https://editor.p5js.org/) will generate a playful name for your first sketch. You can rename your sketch by clicking on the pencil icon above the text editor and typing in a name for your project.  ![Renaming a sketch]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_naming_a_sketch.png?raw=true" | relative_url }}) 
1. Save projects by clicking on File in the top toolbar and selecting Save. Alternatively, you can use the shortcut keys Control+S (PC) or Command+S (Mac).  ![Saving a sketch]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_saving_a_sketch.png?raw=true" | relative_url }})  ![Saved notification]({{ "https://github.com/processing/p5.js-website/blob/main/src/content/tutorials/images/introduction/p5_editor_saved_sketch_notification.png?raw=true" | relative_url }})  

**Tips:** Make sure you are logged in to your account, or you will not be able to save the sketch. Saving projects frequently helps ensure that code isn’t lost if something happens to your computer, browser, or internet connection while you're coding.
{: .notice--success}

### 1E. Sharing, downloading, and deleting your sketches
1. Once your project is saved, you can share it! Click on File in the navigation menu, select Share, and copy one of the links provided to share your project in Embed, Fullscreen, and Edit modes. 
1. If you share your project link with a teacher or classmate, you are giving them the permission to view all of your sketches stored on the [p5.js Editor](https://editor.p5js.org/). This is because all sketches stored in the [p5.js Editor](https://editor.p5js.org/) are publicly viewable. Additionally, it’s also possible for your sketches to show up in search engine results. 
1. There are numerous benefits to projects being shared publicly on the Internet – p5.js programmers can draw inspiration from each other’s creativity and exchange valuable knowledge.
1. However, there are also risks associated with publicly available projects. You should always be cautious about the kinds of personal information you include in your projects, and avoid saving sensitive data, including but not limited to:
    1. Your name
    1. Location
    1. Phone number  
    1. Email address
    1. ID number
    1. Biometric data - this is data that could identify you, like a picture of your face, a sound clip of your voice, etc. Sharing sensitive data like this could put you at risk for dangers like identity theft.
1. If you’d like to remove a sketch from the public’s view, you can download the sketch to your local computer and delete it from your [p5.js Editor](https://editor.p5js.org/) account. Click on File, select Open, find the sketch you hope to remove, then click on the downward triangle arrow on the right-hand side and select Download. 
![p5.js Editor download sketch]({{ "/assets/images/ui/download_sketch_1.png" | relative_url }}) 
![p5.js Editor download sketch]({{ "/assets/images/ui/download_sketch_2.png" | relative_url }}) 
![p5.js Editor download sketch]({{ "/assets/images/ui/download_sketch_3.png" | relative_url }}) 
1. Once the sketch is downloaded to your computer, select "Delete" from the same menu. And voila! You’re now saving your sketches more securely by creating a physical backup of your files on your computer.
1. Interested in learning more about using [p5.js](https://p5js.org/) with a desktop code editor? Check out [Processing Foundation](https://processingfoundation.org/)’s [Setting Up Your Environment tutorial](https://p5js.org/tutorials/setting-up-your-environment/).