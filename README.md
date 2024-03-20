# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


### program:
# Developed By: RAKESH V
# Register Number: 212222110036

## Read image
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('i1.jpg')
Color_image = cv2.imread('i2.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()

## Calculate Hist
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])

## Histogram for Gray image
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

## Histogram for Color image
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

## Histogram Equalization
import cv2
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)

### OUTPUT:

## Input Grayscale Image and Color Image
![image](https://github.com/rakeshcoder2004/Histogram-of-an-images/assets/121490890/425d2c7d-cfb8-4a65-9643-dd9b8c5eb0fc)
![image](https://github.com/rakeshcoder2004/Histogram-of-an-images/assets/121490890/c076e6a6-6263-4615-b5db-5281f9216b63)

## Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/rakeshcoder2004/Histogram-of-an-images/assets/121490890/a0774ea1-5abc-49a9-bc22-e9bd048c8421)
## Histogram Equalization of Grayscale Image.
![image](https://github.com/rakeshcoder2004/Histogram-of-an-images/assets/121490890/1e107f28-10d5-4c10-819e-66a39daab218)

### RESULT:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.


