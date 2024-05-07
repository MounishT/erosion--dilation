# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
## Program:
## DEVELOPED BY: T MOUNISH
## REGISTER NUMBER:212223240098
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'VENKATA RATHNAM',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')






```
## Output:

### Display the input Image
![image](https://github.com/Hariveeraprasad-2006/erosion--dilation/assets/145049988/f5675c81-9cfd-48aa-9961-42f78251cfad)

### Display the Eroded Image
![image](https://github.com/Hariveeraprasad-2006/erosion--dilation/assets/145049988/801d563d-cd87-49cd-a57c-37f983ae9258)

### Display the Dilated Image
![image](https://github.com/Hariveeraprasad-2006/erosion--dilation/assets/145049988/de6b8994-143d-492b-bda0-770a2579060f)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
