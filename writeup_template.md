# **Finding Lane Lines on the Road** 



**Finding Lane Lines on the Road**

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
