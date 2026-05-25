# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step-1:

Create a black image of size 100x600 pixels.
### Step-2:

Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3:

Show the image containing the text without axis labels.
### Step-4:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

## Developed By

**Name:** Amirtha Varshini M


**Register Number:** 212224230017
 
## Program:
```PYTHON
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```PYTHON
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```PYTHON
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```PYTHON
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```PYTHON
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```
```PYTHON
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```PYTHON
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
```PYTHON
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```PYTHON
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```


## Output:

### Display the input Image

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/e5be4e77-9318-45b8-a4be-cf7247729c56" />


### Display the Eroded Image

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/bbb91cb2-24f7-4777-95bd-184498dadc7b" />


### Display the Dilated Image


<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/6a29427e-2eb5-4278-b3fe-46658ce119e3" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
