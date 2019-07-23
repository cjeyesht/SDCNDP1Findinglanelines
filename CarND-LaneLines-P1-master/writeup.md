# **Project:Finding Lane Lines** 

Unlike humans who can identify and decide where to go while driving, an autonomous vehicle has to go through a lot to stick within the lane lines or just to identify the lane lines.This project introduces Computer Vision using python and OpenCV(Open Source Computer Vision). The objective of the project is to identify lane lines on the road. A pipeline is developed on a series of individual images and video stream to indentify lane lines. 


### Setting up the environment 

Requirements : 
1. Python 3 with numpy, matplotlib and OpenCV libraries. 
2. Jupyter Notebook
3. Anaconda python 3 (optional)

Installing OpenCV and other libraries 

>pip install <libraryname>

## Reflections  

### 1. Description

My Pipeline consists of the following 
-  Reading the image and saving a copy
- Grayscale Transform - Converts the image into grayscale
- Gaussian Noise Kernel-Smoothing - Reduces noise
- Canny Transform - Helps in identifying the edges
- Masking the edges - Polygan - Helps in mask the interesting area/region of the image in the shape of polygan
- Hough Transform - Helps in finding the lines on the masked image. It also adjust the lines to have a better two line representation of the lane lines.
- Weighted_img - Helps in merging the image output from the hough transform with the original image
- Resulting image is then plotted

The draw_lines() function is divided into two functions where draw_lines() function is used to find the slope of the points to segment them as right and left line. And the other funciton draw_line() is used to adjust a line or to extrapolate using np.polyfit().



### 2. Identify potential shortcomings/Suggestions with your current pipeline

- Improve masking part so that it could be used commonly for different senarios without any need for altering it. 
- I felt the output of both the videos were good enough. However the output was not as good as the other results as the optional challenge input video involved arc lanes and not straight lines(i.e the car was turning). Further calliberation of the parameters could help to some extent. 
