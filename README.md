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
```py
Developed by: Karthick P
Register Number: 212222100021
```
### Convert image to grayscale and remove noise:
```py
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("eagle.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

```
### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```py
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
```py
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
```py
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```py
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:
```py
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
### SOBEL X AXIS:
![image](https://github.com/karthickprabakaran/EDGE-DETECTION/assets/166775653/3aa43f72-bb39-49f4-88eb-d18c55e8452e)


### SOBEL Y AXIS:
![image](https://github.com/karthickprabakaran/EDGE-DETECTION/assets/166775653/3c9eb1c4-5127-4aa7-aea7-d86e7bc6a639)


### SOBEL XY AXIS:
![image](https://github.com/karthickprabakaran/EDGE-DETECTION/assets/166775653/32bf8a36-dd8a-4292-9ab8-f0c0a5d0572f)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/karthickprabakaran/EDGE-DETECTION/assets/166775653/a32c2920-cd1c-408a-bf25-4d105ed34b1e)


### CANNY EDGE DETECTOR
![image](https://github.com/karthickprabakaran/EDGE-DETECTION/assets/166775653/858dafaf-a2ac-46a3-b50f-0c612c7886b1)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
