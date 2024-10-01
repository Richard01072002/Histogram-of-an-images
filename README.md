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


## Program:
```python
# Developed By: RICHARDSON A
# Register Number: 212222233005

import cv2
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('lkb.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])


```
## Output:
### Input Grayscale Image and Color Image
![lkb](https://github.com/user-attachments/assets/ce0c948c-fa3d-4eae-8281-3c30c36d2c60)

<img width="559" alt="Screenshot 2024-10-01 at 11 38 04 AM" src="https://github.com/user-attachments/assets/0db32a3d-7aab-443a-ab38-9962f24a98e9">


### Histogram of Grayscale Image and any channel of Color Image

<img width="674" alt="Screenshot 2024-10-01 at 11 40 17 AM" src="https://github.com/user-attachments/assets/bb6ff4f1-0184-4eea-b775-b0873281183c">


### Histogram Equalization of Grayscale Image.


<img width="575" alt="Screenshot 2024-10-01 at 11 40 50 AM" src="https://github.com/user-attachments/assets/dc975f42-8627-4774-87cf-f70d71732930">

<img width="630" alt="Screenshot 2024-10-01 at 11 42 43 AM" src="https://github.com/user-attachments/assets/ecb2086a-1837-4165-94b3-6a2f5c4bc9e7">


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
