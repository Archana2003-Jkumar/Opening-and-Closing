# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the packages.
### Step2:
Create a text image.
### Step3:
Create a structuring element.
### Step4:
Do the opening operation.
### Step5:
Do the closing element and the program.
 
## Program:

```
# Import the necessary packages

import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText

text_image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Archana",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'coolwarm')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
imgopen = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.imshow(imgopen)

# Use Closing Operation

imgclose = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.imshow(imgclose)

```
## Output:

### Display the input Image
![image](https://github.com/Archana2003-Jkumar/Opening-and-Closing/assets/93427594/978e3af6-93ee-455e-8144-aed673b55a8c)

### Display the result of Opening
![image](https://github.com/Archana2003-Jkumar/Opening-and-Closing/assets/93427594/e2f7803b-e0f7-4ab5-b225-333314fe17d4)

### Display the result of Closing
![image](https://github.com/Archana2003-Jkumar/Opening-and-Closing/assets/93427594/bbcb0c7d-f9c3-4f9f-b680-95a4f7545ca6)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
