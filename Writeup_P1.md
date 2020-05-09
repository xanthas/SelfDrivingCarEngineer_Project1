# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.
My pipeline consisted of 5 steps:
1. I apply gray scaling as it is an important step.
2. Applied gaussian blur and canny effect to the images
3. Performed edge detection completely then selected regions to search for lane lines
4. Used Hough transform in the operation for the pipeline that actually found line segments in the image and provided the most information of where the lanes lines could be.
5. For this to happen I used the draw line functon to get the lines in y=mx+c form which is a basic line equation.

### 2. Identify potential shortcomings with your current pipeline
The challenge video exposed a couple flaws with my pipeline:
Highly sensitive to color
Requires hard coded regions
Highly dependent on lane location
Also the algorithm did not work as good as I thought it should have worked with bonus challenge.

### 3. Suggest possible improvements to your pipeline
Use information from past frames
Better tuned hough transform and edge detection
Automatically calculate region
Automatically calculate color mask range