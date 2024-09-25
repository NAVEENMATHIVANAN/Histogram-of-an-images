# Histogram-of-an-images
## Aim:
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
# Developed By: Naveen Kumar M
# Register Number: 212222110028
## Input Grayscale Image and Color Image:
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("ajith 2.jpg")
color_image = cv2.imread("thalapathy-vijay.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-09-15 180751](https://github.com/user-attachments/assets/4e805bac-bf31-42f1-b7ac-27b166623cd1)
![Screenshot 2024-09-15 180806](https://github.com/user-attachments/assets/5efd3932-840c-4295-b629-e0f578cee589)

### Histogram of Grayscale Image and any channel of Color Image
```
import cv2
Gray_image = cv2.imread("ajith 2.jpg")
Color_image = cv2.imread("thalapathy-vijay.jpg")
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
## Output:
![Screenshot 2024-09-15 180919](https://github.com/user-attachments/assets/85df6c9a-6906-4e6b-84a3-78c8caddc73c)
![Screenshot 2024-09-15 180931](https://github.com/user-attachments/assets/308ce122-2185-41a4-a8b9-3774e95d37a0)

```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Output:
![Screenshot 2024-09-15 181009](https://github.com/user-attachments/assets/a1108e83-a42b-4104-9dc3-3309fe29276b)
![Screenshot 2024-09-15 181018](https://github.com/user-attachments/assets/7f1ab201-b71d-43ed-8d19-b4219bcff725)

### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("ajith 2.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-15 181136](https://github.com/user-attachments/assets/5f6fac4e-1109-48f6-ba8f-518c71efcfa7)
![Screenshot 2024-09-15 181147](https://github.com/user-attachments/assets/9927b6b2-83f2-40f3-9409-25836538d1c7)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
