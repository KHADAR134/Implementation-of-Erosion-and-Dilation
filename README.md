# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'KHADAR',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image

![10_1](https://user-images.githubusercontent.com/75235233/169857155-d709858e-77c9-4f45-aec1-0869dd79a2b7.png)


### Display the Eroded Image

![10_2](https://user-images.githubusercontent.com/75235233/169857174-f71d3ec0-16a6-45ea-b458-2dc991694258.png)


### Display the Dilated Image

![10_3](https://user-images.githubusercontent.com/75235233/169857202-07e37762-861b-46c4-a58c-9ddd774772ed.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
