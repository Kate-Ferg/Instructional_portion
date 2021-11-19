# Instructional Portion

Just as a little background information, SVG stands for scalable vector graphics. SVGs are useful because they have a smaller file sizes than raster based images, will render clearly no matter the size, and can be styled using CSS. I recommended going through these instructions first using the provided sample material (so skip the "create your own SVG" steps). Then once you feel comfortable, go back through the instructions, but this time try and create your own SVG to use.

## These steps will help you learn how to create a basic SVG animation:

1. First you will need an SVG to work with. You can either create your own digital illustration using Illustrator, or use the SVG I have preloaded into the sample index.html file of this project.

### For creating your own SVG:
First, it is important to note that these instructions will be decribing how to animate a path, so make sure the graphic you create is a line drawing (preferrably made of a single continous path) if you want to follow along closely. If you wish to animate a more complex drawing, it's fine to have multiple paths to animate seperately. There are many other transformations you could explore and apply using shapes such as rotations, fades, translations, scaling, and more, but we will not be touching on those in this project. After going through this exercise, you may want to consider experimenting with some of thpose effects though.
- So to begin, open up Adobe Illustrator and create a graphic. Try to plan ahead of time how you would like your illustration to be animated. This is because each complete shape and path that you make can be animated seperately, so pay attention to each object or layer that you have. 
- Once you have your graphic completed, use the artboard tool to crop the artboard down to fit snuggly against the sides of the illustration.
- You will need to save the file as an SVG now to get the code needed to put into index.html. So go to File > Save As, and then select "SVG" for the format. Click "Save", and then in the next window that pops up you'll want to click the button that says "SVG Code". The code should then open up in a text editor.
- Optionally, you may want to run this code through an SVG optimiser to eliminate unneccessary information, making the code cleaner and quicker to load. To do this you can copy and paste the code into a resourece found at https://jakearchibald.github.io/svgomg/. Just paste the code into the "Paste Markup" area and click the "copy as text" button found right above the download button.
- Now you can paste this text into the sample index.html file of this project (make sure you delete the code for the sample SVG that's already in here).

2. Now you can begin styling the SVG. If using your own SVG, start by adding classes or ids to each individual shape/path you want to animate in index.html. For the sample exercise, we will be animating a line drawing of a girl so that it appears to draw itself. Go ahead and add a class of "line" to the path in index.html.
3. Now you can navigate to the sample styles.css file of the project to begin working on the animation. Select the "line" class that we just added to our path tag. Inside of this selection add: 
```
stroke-dasharray: 7500;
stroke-dashoffset: 7500;
```
These two parameters are what will help us create the line drawing effect. The value of each parameter will increase or decrease depending on how long your path is. The goal is to have one very large stroke that covers the entire path.
4. Directly after the last step, we will declare the animation itself by adding:
```
  animation: draw 25s linear alternate;
```
"Draw" is the name of the animation (you could name it whatever you want). We will be using the name of the animation to reference when adding a keyframe later. "25s" is how long it will take the animation to run from start to finish. You could increase or decrease this value depending on how fast you wan the animation to go. "Alternate"
