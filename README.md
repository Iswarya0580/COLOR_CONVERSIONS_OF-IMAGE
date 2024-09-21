# COLOR_CONVERSIONS_OF-IMAGE

## AIM:
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load an image from your local directory and display it.

### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.

### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.

##### Program:
 
### Developed By:Iswarya P
### Register Number: 212223230082

### 1)Read and Display an Image
```
import cv2
image=cv2.imread('imagee.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('MOON',image)
cv2.waitKey(0)
cv2.destroyAllWindows()  
```
## Output:
![Screenshot 2024-09-13 221341](https://github.com/user-attachments/assets/5c96b209-020e-4a50-8f4d-f2c91f21de2f)


### 2)Draw Shapes and Add Text
```
image=cv2.imread('imagee.jpg')
resr=cv2.rectangle(image,(0,0),(600,600),(0,0,250),12)
cv2.imshow('Result',resr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![alt text](<Screenshot 2024-09-21 132000.png>)
## i)Circle
```
import cv2
img = cv2.imread("imagee.jpg")
res=cv2.circle(img,(320,295),150,(255,0,0),10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 225721](https://github.com/user-attachments/assets/afc1e758-070b-4a17-a8c5-f02073e305a4)

## ii)Line
```
import cv2
img = cv2.imread("imagee.jpg")
res = cv2.line(img,(550,600),(0,0),(0,0,255),10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Selection deleted
## Output:
![alt text](<Screenshot 2024-09-21 140517.png>)

##  iii)Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("imagee.jpg")
text = "Stars and the Moon"
res = cv2.putText(image, text, (10, 50), cv2.FONT_HERSHEY_SIMPLEX, 1, (0,255,0),5)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 230345](https://github.com/user-attachments/assets/6ff1bf4b-330e-4f6c-aeba-3f394a9ecaee)


### 3)Image Color Conversion
```
import cv2
img = cv2.imread('imagee.jpg',1)
cv2.imshow('Original Image',img)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)


gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

YCrCB2 = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCB',YCrCB2)

rgb = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('RGB2YCrCB',rgb)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 231655](https://github.com/user-attachments/assets/e12eca89-c408-464d-a5ca-5ddb7aaf4ed4)

### 4)Access and Manipulate Image Pixels
### (i) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
## Output:
![image](https://github.com/user-attachments/assets/d12550cc-4d5c-4b52-aa05-aec96709b9e3)

### (ii) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('imagee.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 232422](https://github.com/user-attachments/assets/013c2519-52e0-4d15-b7bd-e89accd61646)


### 5)Image Resizing
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 232628](https://github.com/user-attachments/assets/1ad8af5f-845e-4b4a-b4e4-1bd07c3842d7)


### 6)Image Cropping
```

import cv2
image = cv2.imread('imagee.jpg',1)
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 232808](https://github.com/user-attachments/assets/299bb309-6623-4725-b3db-ba221025d2b6)

### 7)Image Flipping
## i)Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("imagee.jpg")
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 232910](https://github.com/user-attachments/assets/05789a64-2f65-4fe1-8a34-552dcc1be184)


## ii)Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("imagee.jpg")
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-09-13 233105](https://github.com/user-attachments/assets/5633af19-2a95-4180-8cbe-49344dc1c82b)



### 8)Write and Save the Modified Image
```
import cv2
img = cv2.imread("image.jpg")
cv2.imwrite('boat_pic.jpg',img)
```
## Output:
![Screenshot 2024-09-13 233227](https://github.com/user-attachments/assets/c5d4b1aa-c1a2-4cbf-bec3-75b46bc8ab5f)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







