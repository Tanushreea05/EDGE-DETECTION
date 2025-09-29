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
### ORIGINAL IMAGE
```
NAME : Tanushree A
REG NO : 212223100057


import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('img.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
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
### ORIGINAL IMAGE:
<img width="738" height="502" alt="Screenshot 2025-09-29 103803" src="https://github.com/user-attachments/assets/c2771590-06a0-4a46-8bbe-44a751ca52da" />

### SOBEL EDGE DETECTOR
<img width="710" height="506" alt="Screenshot 2025-09-29 103812" src="https://github.com/user-attachments/assets/1c3b8ded-d25e-4984-b5f2-22044ffadf26" />



### LAPLACIAN EDGE DETECTOR
<img width="687" height="516" alt="Screenshot 2025-09-29 103819" src="https://github.com/user-attachments/assets/4c8f3b9a-50e6-435b-8f6f-1d511b0ce339" />



### CANNY EDGE DETECTOR
<img width="787" height="497" alt="Screenshot 2025-09-29 103825" src="https://github.com/user-attachments/assets/a8ebbf82-ba30-42fc-8b02-c9330c85dbd2" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
