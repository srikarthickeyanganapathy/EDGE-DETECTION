# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>
### Step2:
Read the image and convert the bgr image to gray scale image.
<br>
### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>
### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>
### Step5:
Display the filtered image using plot and imshow.
<br>

## Program:

```
DEVELOPED BY: S JAIGANESH
REG NO : 212222240037
```
# Import the packages
```
import cv2
import matplotlib.pyplot as pl
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("newo.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
## SOBEL X
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
## SOBEL Y
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
## SOBEL XY
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
# LAPLACIAN EDGE DETECTOR
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

# CANNY EDGE DETECTOR
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
#### SOBEL X
![download](https://github.com/srikarthickeyanganapathy/EDGE-DETECTION/assets/119393842/551be6fb-867b-4f0d-ab32-944097591cd2)

#### SOBEL Y
![download](https://github.com/srikarthickeyanganapathy/EDGE-DETECTION/assets/119393842/2b445ad1-488d-4a53-88f1-bd4df7216059)

#### SOBEL XY
![download](https://github.com/srikarthickeyanganapathy/EDGE-DETECTION/assets/119393842/beb3f1e9-8881-41fd-bb35-156fdd386921)

### LAPLACIAN EDGE DETECTOR
![download](https://github.com/srikarthickeyanganapathy/EDGE-DETECTION/assets/119393842/f2ae5312-3041-4f25-9d1b-f5dc15a24ee4)

### CANNY EDGE DETECTOR
![download](https://github.com/srikarthickeyanganapathy/EDGE-DETECTION/assets/119393842/b1e95a72-69fc-4947-a83f-057c44e4dd05)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
