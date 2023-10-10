# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.
### Step2:
For performing edge detection on a image.
### Step3:
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)

sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)

sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
### Step4:
lap=cv2.Laplacian(gray,cv2.CV_64F)
### Step5:
canny=cv2.Canny(gray,120,150)
Display all the images with their respective edge detected images.
## Program:

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("alian.jpeg",0)
photo=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
photo=cv2.GaussianBlur(photo,(3,3),0)
cv2.imshow("baskaran_212222230020",photo)
cv2.waitKey(0)

# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(photo,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(7,7))
plt.subplot(1,2,1)
plt.imshow(photo)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(photo,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.imshow(photo)
plt.title("Original image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(photo,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(7,7))
plt.subplot(1,2,1)
plt.imshow(photo)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()


# LAPLACIAN EDGE DETECTOR

lap=cv2.Laplacian(photo,cv2.CV_64F)
plt.figure(figsize=(10,8))
plt.subplot(1,2,1)
plt.imshow(photo)
plt.title("Original image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("LAPLACIAN EDGE DECTECTOR")
plt.axis("off")
plt.show()

# CANNY EDGE DETECTOR
canny=cv2.Canny(photo,120,150)
plt.figure(figsize=(7,7))
plt.subplot(1,2,1)
plt.imshow(photo)
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
![download](https://github.com/BaskaranV15/EDGEDETECTION/assets/118703522/c128fee4-6363-487a-896e-e3c685e31a9e)




### LAPLACIAN EDGE DETECTOR


### CANNY EDGE DETECTOR


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
