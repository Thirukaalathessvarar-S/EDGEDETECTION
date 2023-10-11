# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.

### Step2:
Read the image and convert the rgb image to gray scale image.

### Step3:
Use filters for smoothing the image to reduce the noise.

### Step4:
Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
Display the filtered image using plot and imshow.
 
## Program:
```
Developed by : Thirukaalathessvarar S
Reg no : 212222230161
```

### Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

### Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("cat.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR

#### SOBEL X
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

#### SOBEL Y
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

#### SOBEL XY
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
plt.title("Original Image")b
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
### SOBEL EDGE DETECTOR
![dip_exp7_1](https://github.com/Thirukaalathessvarar-S/EDGEDETECTION/assets/121166390/15a2ecf8-5f2a-48db-8260-363198b1993a)

![dip_exp7_3](https://github.com/Thirukaalathessvarar-S/EDGEDETECTION/assets/121166390/1a6f5119-9bc6-4c89-87d5-9866a876ba15)

![dip_exp7_4](https://github.com/Thirukaalathessvarar-S/EDGEDETECTION/assets/121166390/99343d17-0ea3-410d-a653-d900c8db12fe)

### LAPLACIAN EDGE DETECTOR
![dip_exp7_5](https://github.com/Thirukaalathessvarar-S/EDGEDETECTION/assets/121166390/6f12eeaf-e6fe-441f-b464-ddc709c0f1ea)

### CANNY EDGE DETECTOR
![dip_exp7_6](https://github.com/Thirukaalathessvarar-S/EDGEDETECTION/assets/121166390/0a9ff41f-d273-49f1-887d-db4d09e136e9)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
