---
# This is the frontmatter
title: "Sample Unit Page" # Title and Heading 1
permalink: /unit-sample/ # Give your page a permalink
hidden: true # Remove this line for any units you want added to the sidebar navigation

gallery: # Below is for including an image gallery
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 1 title caption"
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 2 title caption"
  - url: /assets/images/sample-img.jpg
    image_path: /assets/images/sample-img.jpg
    alt: "Soft gradient with pinks and greens"
    title: "Image 3 title caption"

---

This is a sample unit page. You'll find this page in the `_curriculum` directory, but it's not rendered in curriculum the sidebar navigation.

Files in the `_curriculum` directory are written in Markdown, and file names follow the format `number-unit.md`, where the number will determine the pagination order.

For more info on syntax, check out this [Markdown Guide](https://www.markdownguide.org/tools/jekyll/)!

## Minimal Mistakes Theme

This site uses a customized version of the Minimal Mistakes theme. You can read more about it at the [Minimal Mistakes Documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/).

## Table of Contents

The table of contents on the right is auto-generated using the [headings]([heading levels](https://www.markdownguide.org/basic-syntax/#headings)) on the page. To generate the table of contents properly, [headings should follow a logical order](https://www.w3.org/WAI/tutorials/page-structure/headings/#heading-ranks) (Heading 3 is nested under Heading 2, etc.).

## Formatting Options

Below are examples of formatting options you may want to use.

### Code Snippets

**Code blocks** are created as follows:

```js
// Here's a code block with JavaScript syntax highlighting
function setup() {
    consoloe.log('Hello world!');
}
```

### Images

**Images** can be added to the `/assets/images/` directory.

![Soft gradient with pinks and greens]({{ "/assets/images/sample-img.jpg" | relative_url }})

You can also create a `<figure>` element with a caption:

{% include figure popup=true image_path="/assets/images/sample-img.jpg" alt="Soft gradient with pinks and greens" caption="This is a figure caption." %}

You can also create a [gallery of images](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#gallery) (you will need to include the corresponding gallery frontmatter at the top of the page):

{% include gallery caption="This is a sample gallery with **Markdown support**." %}


