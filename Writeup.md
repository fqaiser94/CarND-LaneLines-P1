# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/solidWhiteCurve.png "solidWhiteCurve"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of the following steps:   
- Convert image to grayscale 
- Apply Gaussian Blur to smoothen edges
- Apply Canny Edge Detection to detect edges
- Extract only edges in our region Of interest
- Perform a Hough Transform to find lanes
- Separate left and right lanes
- Find lines of best fit for both left and right lanes
- Overlay lines over original image

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the image's centre is not aligned with the middle of the lane, which is something my function assumes.   

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use the gradient of the lines detected to seperate them into left and right lane lines. While I attempted to do this, the resulting left and right lane lines were quite jerky during video.   