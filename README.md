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
```
import cv2
import matplotlib.pyplot as plt

# Read the image
img = cv2.imread('image.jpg')  # TYPE THE CODE HERE TO READ THE IMAGE USING IMREAD

# Convert the color to gray
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)  # CONVERT THE COLOR TO GRAY TO RGB
gray = cv2.GaussianBlur(gray, (3, 3), 0)

# Sobel X
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# Sobel Y
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)  # TYPE THE CODE HERE
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

# Sobel XY
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
# TYPE THE CODE HERE
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# Laplacian
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(lap, cmap='gray')  # DISPLAY THE IMAGE USING IMSHOW
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# Canny
canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")  # PROVIDE THE TITLE OF THE IMAGE DISPLAYED PAGE
plt.axis("off")
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
<img width="639" height="411" alt="image" src="https://github.com/user-attachments/assets/1088924a-3b2b-4a00-af82-17fd8c4d1d94" />
<img width="639" height="411" alt="image" src="https://github.com/user-attachments/assets/3e1d7e0f-fb1f-4ffb-8a3f-bda09e10aef6" />
<img width="639" height="411" alt="image" src="https://github.com/user-attachments/assets/53851c7c-eba3-4d4f-9e43-8318e32e2a80" />


### LAPLACIAN EDGE DETECTOR
<img width="639" height="411" alt="image" src="https://github.com/user-attachments/assets/8797be72-cc50-4fdd-9c39-7aaa8e13eaf0" />



### CANNY EDGE DETECTOR
<img width="639" height="411" alt="image" src="https://github.com/user-attachments/assets/08052bd8-ccad-4242-ad73-fe6a9654f1fa" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
