# Finding-distance-between-objects-in-an-image-using-OpenCV
It is very difficult for getting a perfect distance between gaps and objects, Here using OpenCV, some possibilities can be made

Actually there are certain requirements
1) Scipy
2) imutils
3) numpy
4) argparse // to get input from user while running
5) OpenCV

Or 

Directly downloading Anaconda from https://www.anaconda.com/download/ will automatically download certain libraries that are widely used


So, Steps involved

1) Read an image
2) perform edge detection
3) then perform a dilation + erosion to close gaps in between object edges
4) find contours in the edge map
5) sort the contours from left-to-right and initialize the 'pixels per metric' calibration variable
6) compute the rotated bounding box of the contour
7) order the points in the contour such that they appear in top-left, top-right, bottom-right, and bottom-left order, then draw the outline of the rotated bounding box
8) compute the midpoint between the top-left and top-right points, followed by the midpoint between the top-righ and bottom-right
9) draw lines between the midpoints to show the output
