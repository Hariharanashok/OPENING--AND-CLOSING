# OPENING-AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
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
### Import the necessary packages
```python
import cv2
import numpy as np
```

### Create the Text using cv2.putText
```python
# Create the original image with text
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Hariharan A', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
small_img = cv2.resize(img, (700, 175))  # Resize dimensions as (width, height)
cv2.imshow('Original Image', small_img)
cv2.waitKey(0)
```

### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))  # Adjust size as needed
```

### Use Opening operation
```python
opening_img = cv2.morphologyEx(small_img, cv2.MORPH_OPEN, kernel)
cv2.imshow('Opening Operation', opening_img)
cv2.waitKey(0)
```

### Use Closing Operation
```python
closing_img = cv2.morphologyEx(small_img, cv2.MORPH_CLOSE, kernel)
cv2.imshow('Closing Operation', closing_img)
cv2.waitKey(0) # Final common
cv2.destroyAllWindows()
```

## Output:
### Display the input Image
![Orignal](https://github.com/user-attachments/assets/da991de4-68c7-4e62-8029-d7dee5c37d98)


### Display the result of Opening
![Opening](https://github.com/user-attachments/assets/1295efb4-cb13-4d7d-a001-56eb6d344113)


### Display the result of Closing
![Closing](https://github.com/user-attachments/assets/d3789d02-e260-43cf-b662-ac325cf30b60)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
