# EDGE-DETECTION

### Developed By: YUGABHARATHI M
### Reg.No: 212224230314

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

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('Tiger.jpg')  # Replace with your image path
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

## OUTPUT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

<img width="644" height="505" alt="image" src="https://github.com/user-attachments/assets/42bff1cd-960c-41ed-8a9a-fd0dd416145f" />
<img width="639" height="500" alt="image" src="https://github.com/user-attachments/assets/9bc0e6eb-46f5-4dc8-b00a-a4a48a9977a8" />
<img width="697" height="548" alt="image" src="https://github.com/user-attachments/assets/5d5dea52-e8fa-4361-8dfb-92d1f5fa1881" />
<img width="652" height="510" alt="image" src="https://github.com/user-attachments/assets/db4b2fac-4fa4-4328-ba6f-5da4a7610dce" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
