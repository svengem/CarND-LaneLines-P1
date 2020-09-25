# **Finding Lane Lines on the Road** 


### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The goal of the project is to develop a pipeline that can be used to detect lane lines in an image/video.  The pipeline is written in Python using OpenCV. The project consists of two files. The file P1.ipynb with the code and README.md with the description.

My pipeline consisted of the following steps: 

- Converting image to grayscale
- Appllying Gaussian Blur to the image
- Applying Canny edge detection
- Filter out region of interest
- Houghlines outputs a list of line segments
- I modified the draw_lies funciton by sorting the lines by slope (left/right). Then it calculates the mean. At the end the weighted average over time is used to avoid flickering.

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming is that it only works well for straight lines. The Pipeline also has problems detecting lines with different colors like shadows etc.
Another shortcoming is roads with ascending and descending slopes, because the algorithm assumes the visible end near the middle oft the image.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use Plyfit to better detect curvy lane lines.
Another potential improvement could be to use variable Parameters for region of interest, gaussian smoothing etc. because they may change for different driving situations.
There might be better algorithms to detect lane lines with different color (shadows, etc.)
