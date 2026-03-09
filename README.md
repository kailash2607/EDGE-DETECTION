# Exp-6
# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

### Developed by: KAILASH PRABHU S
### Register Number: 212224240068

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('k12.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
<img width="693" height="533" alt="image" src="https://github.com/user-attachments/assets/014c4a97-0d66-424a-a8c1-dcbae04c1866" />

<img width="772" height="547" alt="image" src="https://github.com/user-attachments/assets/8f357f88-dc02-4a2c-a3f0-db13af72d354" />

<img width="691" height="550" alt="image" src="https://github.com/user-attachments/assets/1e506d7b-dc0b-43c9-800f-adfcec91ff95" />

<img width="702" height="532" alt="image" src="https://github.com/user-attachments/assets/0c6fb5c8-2634-451f-9f94-2b9aefada450" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
