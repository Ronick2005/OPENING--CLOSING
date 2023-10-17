# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening operation.
### Step5:
Use Closing Operation.
 
## Program:
# Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Ronick Aakshath', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```python
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```python
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/Ronick2005/OPENING--CLOSING/assets/83219341/8e8d0723-6899-48c0-9b69-a8e2946b82ca)

### Display the result of Opening
![image](https://github.com/Ronick2005/OPENING--CLOSING/assets/83219341/e10dcfb0-acda-4b12-99d3-d05c94915b6b)

### Display the result of Closing
![image](https://github.com/Ronick2005/OPENING--CLOSING/assets/83219341/5fd7ed9f-de54-4e20-a6b2-656cb8b959c9)

## Result
Thus the Opening and Closing operation is used in the image using Python and OpenCV.
