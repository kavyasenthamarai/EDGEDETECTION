# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the required packages for further process.

### Step 2:
Read the image and convert the bgr image to gray scale image.

### Step 3:
Use any filters for smoothing the image to reduse the noise.

### Step 4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:
Display the filtered image using plot and imshow.

## Program:
``` 
DEVELOPED BY : Kavya K
REG NO : 212222230065
```

# Import the packages ,Load the image, Convert to grayscale and remove noise
``` python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("eye.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
# SOBEL X AXIS :
``` python
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
# SOBEL Y AXIS :
``` python
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
# SOBEL XY AXIS :
``` python
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
# LAPLACIAN EDGE DETECTOR
``` python
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
# CANNY EDGE DETECTOR
``` python
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
### SOBEL X AXIS :
![image](https://github.com/MukeshVelmurugan/EDGEDETECTION/assets/118707363/2dfe842a-bb24-441e-a160-62bc109ac6c1)


### SOBEL Y AXIS :
![image](https://github.com/MukeshVelmurugan/EDGEDETECTION/assets/118707363/c352daa3-8374-45b2-b036-cdef5a82b1a1)


### SOBEL XY AXIS :
![image](https://github.com/MukeshVelmurugan/EDGEDETECTION/assets/118707363/88f034bf-ee1b-4560-9976-a9303fadbe28)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/MukeshVelmurugan/EDGEDETECTION/assets/118707363/35c4b177-77ea-4560-b18b-2b9b7c34e4d4)


### CANNY EDGE DETECTOR
![image](https://github.com/MukeshVelmurugan/EDGEDETECTION/assets/118707363/144c306e-929b-42aa-a1e7-2496baf8deec)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
