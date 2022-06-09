# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages for implementing the code.

### Step2:
Create the text that you want to modify using opening and close filter.

### Step3:
Create the structuring element that you want to use over the image.

### Step4:
Apply the opening and closing operation for the original image.

### Step5:
Show the results using imshow function from cv2.
 
## Program:

``` Python
# Developed by: B Mahalakshmi.
# Reg.No.: 212221240008
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_SCRIPT_COMPLEX
im=cv2.putText(img,' Pavan GV ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(cv2.cvtColor(im, cv2.COLOR_BAYER_GR2BGRA))

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(cv2.cvtColor(image1, cv2.COLOR_BAYER_GR2BGRA))

# Use Closing Operation
image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(cv2.cvtColor(image1,cv2.COLOR_BAYER_GR2BGRA))




```
## Output:

### Display the input Image
![11 1M](https://user-images.githubusercontent.com/93427286/172935078-de1aedfc-3d6e-4e29-a372-6be0340918de.png)

### Display the result of Opening
![11 2M](https://user-images.githubusercontent.com/93427286/172935075-4b2c4b1f-3738-4178-9c8b-cdb0a0673d8d.png)

### Disp![11 3M](https://user-images.githubusercontent.com/93427286/172935067-b14b24bb-14a0-48dd-af62-080fc495e13e.png)
lay the result of Closing

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
