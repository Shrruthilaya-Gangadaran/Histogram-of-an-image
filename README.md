# HISTOGRAM AND HISTOGRAM EQUALIZATION OF IMAGE
## AIM:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step4:
cv2.equalize() is used to transform the gray image to equalized form.

### Step5:
The Histogram of gray scale image and color image is shown.
## PROGRAM:
Developed By : Shrruthilaya G

Register Number : 212221230097
### Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt

gray = cv2.imread('friends1.webp')
color= cv2.imread('friends2.webp')
plt.imshow(gray)
plt.show()
plt.imshow(color)
plt.show()
```
### Display the histogram of gray scale image and any one channel histogram from color image.
```
gray_hist = cv2.calcHist([gray],[0],None,[256],[0,255])
plt.figure()
plt.title("Histogram GRAY")
plt.xlabel("grayscale value")
plt.ylabel("pixelcount")
plt.stem(gray_hist)
plt.show()

color_hist = cv2.calcHist([color],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram COLOR")
plt.xlabel('color value')
plt.ylabel('pixel count')
plt.stem(color_hist)
plt.show()
```
### Write the code to perform histogram equalization of the image. 
```
import cv2
gray=cv2.imread('friends1.webp',0)
equ = cv2.equalizeHist(gray)
cv2.imshow('GRAY IMAGE',gray)
cv2.imshow('EQUALIZED IMAGE',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
### Input Grayscale Image and Color Image
![](https://github.com/Shrruthilaya-Gangadaran/Histogram-of-an-image/blob/main/output1.png)
### Histogram of Grayscale Image and any channel of Color Image
![]([output2.png](https://github.com/Shrruthilaya-Gangadaran/Histogram-of-an-image/blob/main/output2.png))
### Histogram Equalization of Grayscale Image
![]([output3.png](https://github.com/Shrruthilaya-Gangadaran/Histogram-of-an-image/blob/main/output3.png))

## RESULT: 
Thus, the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
