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

    1. Convert the image to grey scale we do this because edge detection will not require the color information 
    2. Then apply Gaussian function for noise reduction in the image 
    3. Pass the Gaussian blured image to a canny edge detector with upper and lower threshold values this double thresholding  helps in detecting only the images required 
    4. the image is then cropped so that the mask applied will hide all other edges except for that of the lane 
    5. this masked image is then hough transformed for full feature extraction is , An image with lines drawn on
    
-----

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by

    1. reshaping the lines fit to a 2d matrix
    2. then creating an array of slopes
    3. remove nan and infinity from the lists
    4. converting lines into list of points
    5. moving all points with negative slopes into right "lane"
    6. moving all points with negative slopes into left "lane"
    7. calculate polynomial fit for the points in each lane
    8. use new curve function f(y) to calculate x values
    

   

