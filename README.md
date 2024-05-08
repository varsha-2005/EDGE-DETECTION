# EX-06 EDGE-DETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

## Step1:
Import all the necessary modules for the program.
## Step2:
Load a image using imread() from cv2 module.
## Step3:
Convert the image to grayscale
## Step4:
Using Sobel operator from cv2,detect the edges of the image.
## Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Programs

Developed By:Varsha G
Reg.No:212222230166


## Original Image
![WhatsApp Image 2024-04-02 at 23 01 43_9bb87855](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/1d7824aa-cf69-4764-9b79-2103ce55400f)


### Convert image to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("fox.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR

### SOBEL X AXIS :
```
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
```
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
```
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
### LAPLACIAN EDGE DETECTOR
```
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
### CANNY EDGE DETECTOR
```
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

SOBEL EDGE DETECTOR

Sobel X Axis Edge Detection

![image](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/fbb10a9f-da2b-4556-adf3-f974017d3818)


Sobel Y Sxis Edge Detection

![image](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/15d96408-2806-4c32-ad61-3464a61afc78)


Sobel XY Sxis Edge Detection

![image](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/d6ef2ce5-fcab-4560-aba2-a0c536848f00)


LAPLACIAN EDGE DETECTOR

![image](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/41f721a0-c9d0-4d65-83dd-1f18b0e95553)



CANNY EDGE DETECTOR

![image](https://github.com/niraunjana/EDGE-DETECTION/assets/119395610/669bcc45-a395-4cf2-a784-04264bc2b377)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
