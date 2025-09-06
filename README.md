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
# Developed By: Priya Varshini P
# Register Number: 212224240119
import cv2
import matplotlib.pyplot as plt 
Gray_image=cv2.imread("Eagle_in_Flight_Grayscale.png")
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread("eagle_in_Flight.jpg")
plt.imshow(Color_image)
plt.show()
# Write your code to find the histogram of gray scale image and color image channels.
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value') 
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image.

equ1=cv2.equalizeHist(cv2.imread('eagle_in_Flight.jpg',0)) 
equ=cv2.cvtColor(equ1,cv2.COLOR_BGR2RGB) 
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ) 
plt.show()

```
## Output:
### Input Grayscale Image and Color Image
![dipexp3op1](https://github.com/user-attachments/assets/262e828d-52a8-499e-b595-8d5a9de3067e)


![dipexp3op2](https://github.com/user-attachments/assets/e42d22ac-d281-4a7b-96b4-cf5736cdccca)


### Histogram of Grayscale Image and any channel of Color Image

![dipexp3op3](https://github.com/user-attachments/assets/a757f30b-d924-45e4-8796-c614f0c29c13)

![dipexp3op4](https://github.com/user-attachments/assets/3ef0fff0-9257-4480-b05f-b652f84942da)


### Histogram Equalization of Grayscale Image.

![dipexp3op5](https://github.com/user-attachments/assets/0ad328be-dd69-4a6a-8ba1-073ab0c06ceb)

### Result:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
