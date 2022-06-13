InkSlide
========

Part of my Zero-Microsoft by 2030 pledge.

The latest release of Inkscape includes pages. This opens the door to using Inkscape to create slides for presentations.


![Turn svg pages into slides](img/cover.png)

This repository contains two key files:

- `slides.svg` - the content of the slides as edited with Inkscape
- `index.html` - the file to open in your browser to present `slides.svg`

Requirements
------------
Both files should be placed in a folder that can be served as a localhost webpage. Opening `index.html` as a file will not give access to the content of the svg file (for security reasons).
On a Mac, try the `Sites` folder. You may have to configure the folder (let me know if that is painful and I can include some steps here).

Editing the svg
---------------

Use Inkscape (v1.2+) to edit `slides.svg`.

**SVG id**: if you create a new file, make sure the `id` for the svg element is set to `svgSlides`. You can do this directly in the XML editor at the very top (`<svg:svg id="svgSlides">`).

**Page order**: Inkscape has a feature to reorder pages, but that is rather clunky. InkSlide therefore reorders them in the order they appear in the Inkscape workspace. Note that if you export your slides as pdf, they will be in the Inkscape order (I hope Inkscape will add a feature 'order pages by position' at some point).

**Animation**: Elements can be shown and hidden on slides. Add a `class` to any element (or group) and set the value to `show1`. Class names have to be sequential (show1..10). These will appear after n advances on the slide. Elements with `hide1` (or any number 1-10), disappear at that point. One element can have multiple classes, such as `class = 'show2 hide3 show4'` to emerge, disappear and come back.

**Navigation**: At the bottom of the slides is a strip with slide numbers names. The page name is shown if specified in Inkscape. Green icons indicate that this slide has been visited. The current slide has a white border. Click on any slide indicator to jump directly to that slide.

![Pages with a name show up in the navigation bar. Others are numbered](img/page_name.png)

Presenting
----------

Open `index.html` in your browser and switch to full screen. The first slide advance has to be done by clicking anywhere on the slide. 

After that, `<Space>` and `<ArrowRight>` also advance the slides. 

`<ArrowLeft>` goes back.

Jump directly to a slide by clicking on the navigation bar.

`All` brings up and overview of all slides.

![`All` opens an overview](img/all.png)
