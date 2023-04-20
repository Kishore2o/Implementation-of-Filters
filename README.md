# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().

### Step2

Convert the saved BGR image to RGB using cvtColor().
### Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

### Step4
Apply the filters using cv2.filter2D() for each respective filters.

### Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program:
### Developed By   : KAVINRAJA D
### Register Number: 212222240047


### 1. Smoothing Filters
```
i) Using Averaging Filter
Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```



ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()


```



iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```




iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```




### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```





ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```




## OUTPUT:
### 1. Smoothing Filters
## i) Using Averaging Filter
![imp](https://user-images.githubusercontent.com/118679883/233408088-ab482275-034d-4411-ab13-010ce373564b.jpg)


## ii) Using Weighted Averaging Filter
![imp 2](https://user-images.githubusercontent.com/118679883/233408228-e3147a52-ee1c-4ac2-854b-8e49c9a3f66d.jpg)


## iii) Using Gaussian Filter
![imp 3](https://user-images.githubusercontent.com/118679883/233408282-434c9eaa-f60b-430a-b24c-51f8f3bb25c5.jpg)


## iv) Using Median Filter
![img 4](https://user-images.githubusercontent.com/118679883/233408335-67208b99-7329-4903-b843-0ba796e461a1.jpg)


### 2. Sharpening Filters
## i) Using Laplacian Kernal
![img 5](https://user-images.githubusercontent.com/118679883/233408402-14d3f372-d5b8-4305-b397-12bf95212c55.jpg)


## ii) Using Laplacian Operator
![imp 6](https://user-images.githubusercontent.com/118679883/233408477-644a7a7e-a503-4618-b0bd-743b2a98489a.jpg)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
