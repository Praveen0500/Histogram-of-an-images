# Histogram of images
## Aim
### To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
### Anaconda - Python 3.7

## Algorithm:
### Step1:
#### Read the gray and color image using imread()

### Step2:
#### Print the image using imshow().

### Step3:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
#### The Histogram of gray scale image and color image is shown.


## Program:

### Colour and Gray Image

# Developed By: PRAVEEN S
# Register Number: 212222240078
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpeg")
color_image = cv2.imread("co;our.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image

```py
import numpy as np
import cv2
Gray_image = cv2.imread("Gray.jpeg")
Color_image = cv2.imread("colour.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

### Histogram of Green channel of colour Image

```py
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```



```py

import cv2
gray_image = cv2.imread("colour.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:

### Input Grayscale Image and Color Image

![Screenshot 2024-03-05 220714](https://github.com/Praveen0500/Histogram-of-an-images/assets/120218611/205d8e28-436f-42f9-a03c-057e65fc5619)

### Histogram of Grayscale Image

![Screenshot 2024-03-05 220941](https://github.com/Praveen0500/Histogram-of-an-images/assets/120218611/8e8844dd-46ee-4542-8474-c88734115b0a)


### Histogram of Green Channel of colour Image

![Screenshot 2024-03-05 221250](https://github.com/Praveen0500/Histogram-of-an-images/assets/120218611/e282763d-6c52-4e58-9344-c5ccd2122c12)



### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-05 221446](https://github.com/Praveen0500/Histogram-of-an-images/assets/120218611/7c0eec3d-9c79-4016-96a4-2b124ae0a5e9)



## Result: 
### Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
