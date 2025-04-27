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
Developed by: Sanjay Balaji S
Register Number: 212223240149
```
### Convert image to grayscale and remove noise:
```py
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("spiderman.jpeg",0)
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
![image](https://github.com/user-attachments/assets/160ecada-9ac7-4292-8421-553fe12ff304)

### SOBEL Y AXIS:
![image](https://github.com/user-attachments/assets/2e6c83cf-7ef2-4ca6-afb4-f0e6418fd00c)

### SOBEL XY AXIS:
![image](https://github.com/user-attachments/assets/1aec5522-dcf4-4ffe-8925-3de7f05126e9)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/b397d8bf-ab76-4ac5-948c-dfac115b8c2e)

### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/35290773-e58d-4476-8893-72a272116dd3)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
