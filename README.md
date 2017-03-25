# [![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/sdc-banner-medium-1170_660.png)](http://www.udacity.com/drive)
# Udacity - Self-Driving Car NanoDegree - Project 1 

**Finding Lane Lines on the Road**

[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---
### Goals

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report
----

### Reflection

the pipeline consisted of the following steps 
1. Convert the image to grey scale we do this because edge detection will not require the color information 
2. Then apply Gaussian function for noise reduction in the image 
3. Pass the Gaussian blured image to a canny edge detector with upper and lower threshold values this double thresholding helps in detecting only the images required 
4. the image is then cropped so that the mask applied will hide all other edges except fot that of the lane 
5. this masked image is then hough transformed for full feature extraction is , An image with lines drawn on it.
