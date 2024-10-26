# EX-10:OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Read the Image:
Load the input color image from a specified path.

### Step-2:Convert to Grayscale:
Transform the color image into a grayscale format for easier processing.

### Step-3:Edge Detection:
Apply an edge detection technique to identify the prominent edges in the grayscale image.

### Step-4:Create Structuring Element:
Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.

### Step-6:Morphological Operations:
Perform morphological operations:<br>
Opening: Remove small objects from the edges to clean up the image.<br>
Closing: Fill small holes in the detected edges to enhance the structure.

### Step-7:Display Results:
Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.

## Program:
```
Developed By : K.R.Hashish Vidya Sagar
Register Number: 212222230047
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the structuring element
```
image = cv2.imread("Fish.jpg")
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
# Convert images from BGR to RGB for Matplotlib
```
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
```
# Plot the original, opening, and closing images using Matplotlib
```
plt.figure(figsize=(10, 5))


plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")


plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")


plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```

# OUTPUT:
# Original Image
![image](https://github.com/user-attachments/assets/7872fc5e-539e-45e1-9f84-2f8f196d8143)

# Opening Operation:
![image](https://github.com/user-attachments/assets/9b765bf9-8ce0-4a4e-8d46-f90e8cdfc1b8)
# Closing Operation:
![image](https://github.com/user-attachments/assets/e699e6ab-a06f-4933-8777-27133fa821b3)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
