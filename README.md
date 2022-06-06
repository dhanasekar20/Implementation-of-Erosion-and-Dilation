# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.
 
## Program:
```
/*
Developed by   : DHANASEKAR.G
Register Number: 212220230009
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,700),dtype='uint8')
font=cv2.FONT_ITALIC=3
img2=cv2.putText(img1,"Kumaran",(5,70),font,3,(255),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernal1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erode=cv2.erode(img2,kernel)
cv2.imshow("Erosion1",erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
dilute=cv2.dilate(img2,kernel1)
cv2.imshow("Dilution",dilute)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image


![zx](https://user-images.githubusercontent.com/75264748/172203967-55b21c46-4bca-41cd-a3a0-5e380abda811.jpg)


### <br><br>Display the Eroded Image
![zx1](https://user-images.githubusercontent.com/75264748/172203973-a06a3b32-4b8b-4b42-8ae1-345b440ea9de.jpg)



### Display the Dilated Image
![zx3](https://user-images.githubusercontent.com/75264748/172203993-14935e28-fdd7-44f8-949f-8fb188f1443c.jpg)


## <br><br><br><br>Result
Thus the generated text image is eroded and dilated using python and OpenCV.
