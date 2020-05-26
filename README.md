# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road



[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---
### How To run

Please review the installation instructions [here](https://github.com/udacity/CarND-LaneLines-P1/blob/master/README.md)

**Finding Lane Lines on the Road**

The goal of this project is to:
* Make a pipeline that finds lane lines on the road


[//]: # (Image References)

[image1]: ./result_images/solidWhiteCurve.jpg "solidWhiteCurve"
[image2]: ./result_images/solidWhiteRight.jpg "solidWhiteRight"
[image3]: ./result_images/solidYellowCurve.jpg "solidYellowCurve"
[image4]: ./result_images/solidYellowCurve2.jpg "solidYellowCurve2"
[image5]: ./result_images/solidYellowLeft.jpg "solidYellowLeft"
[image6]: ./result_images/whiteCarLaneSwitch.jpg "whiteCarLaneSwitch"

---

### Reflection

### 1. Pipeline Description 

This pipeline consisted of 6 steps:
* Reading image from an array of images
* Converting the images to grayscale
* Applying Gaussian smoothing Module(5,5) kernel
* Using Canny Edge Detection Module 
* Selecting the region of interest, Ego lane
* Applying Hough Tranform line detection
* Blending our hough transform and image.

In order to draw a single line on the left and right lanes, I written the draw_lines2() function by getting the lines' slopes

![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]
![alt text][image5]
![alt text][image6]


### 2. Potential shortcomings with the current pipeline


* As Canny edge detector works on Image gradient which is slower, rather be workef upon itensity if images directly.


### 3. Possible improvements to the current pipeline

* Challenging part is shows that code doesn't work for  curvy lanes should be worked on. It shows the straight lines on curves
