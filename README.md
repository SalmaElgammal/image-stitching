# Image Stitching

Using image warping and homographies, an image mosaic is created.

## Getting started

### Prerequisites

To run this appliction. You need to install python, cv2 and numpy

### Running a test case

1. Run main.py using the command
   ```
   python main.py
   ```
2. Two images will show up. Use the mouse to define correspondences. Click on any pixel in the first image then click on the corresponding pixel on the second image. You have to define at least 4 correspondences (8 clicks). The more pixels you define, the more accurate result you will get
3. Press any key and wait until the output image appears (this may take a while).
4. Press any key to close the output image.

### Using your own image

To use other images:

1. copy the images you want to the current directory.
2. Change main.py lines 6 and 7 to the new image names

## Sample Runs

### Input images

![Left image](left.jpg)
![Right image](right.jpg)

### Output image

![Left image](output.png)

## How it works

Mouse clicks are stored in two arrays: `imgClicks1` and `imgClicks2`. These two arrays are used to compute the homography matrix. A homography matrix maps any pixel position in the left image to its corresponding position in the right image.
This matrix is then used to estimate the new pixels locations. The output is the warped right image concatenated with the original left image
