# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

To complete the project, two files will be submitted: a file containing project code and a file containing a brief write up explaining your solution. We have included template files to be used both for the [code](https://github.com/udacity/CarND-LaneLines-P1/blob/master/P1.ipynb) and the [writeup](https://github.com/udacity/CarND-LaneLines-P1/blob/master/writeup_template.md).The code file is called P1.ipynb and the writeup template is writeup_template.md 

To meet specifications in the project, take a look at the requirements in the [project rubric](https://review.udacity.com/#!/rubrics/322/view)


Creating a Great Writeup
---
For this project, a great writeup should provide a detailed response to the "Reflection" section of the [project rubric](https://review.udacity.com/#!/rubrics/322/view). There are three parts to the reflection:

1. Describe the pipeline
    -Convert image to grayscale with white/yellow line masked image
    <img src="test_images_output/HLS.jpg" width="480" alt="HLS" />
    -convert grayscale image to canny edge image with gaussian blur
    <img src="test_images_output/canny.jpg" width="480" alt="canny" />
    -Identify interested area for our lanes and mask other regions with black color
    -From the masked image, identify the lanes using Hough method and mask hough lines on it.
    <img src="test_images_output/regionandHoughlines.jpg" width="480" alt="regionandHoughlines" />
    -Merge original images with Hough lines
    <img src="test_images_output/houghLines.jpg" width="480" alt="houghLines" />
    -Run it through the image

2. Identify any shortcomings
    -The Challenge part of the image is still not getting left lane lines. This has to be investigated in due course of time.
    -Curved lanes can be integrated. This will require further investigation and effort but can be done.
    -There are moment where the lines are flickering, The reason for this needs to be found out
    
3. Suggest possible improvements
    - The Challenge part of the video is still not getting left lane lines. This has to be investigated.



