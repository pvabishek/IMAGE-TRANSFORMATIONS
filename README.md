# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1: 
 Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:
1. Translation moves the image along the x or y-axis.
2. Scaling resizes the image by scaling factors.
3. Shearing distorts the image along one axis.
4. Reflection flips the image horizontally or vertically.
5. Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.

## Program:
#### Developed By: ABISHEK PV
#### Register Number: 212222230003
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('image4.jpg')
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
```
## i)Image Translation
```
# 1. Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```

## ii) Image Scaling
```
# 2. Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off
```
## iii)Image shearing
```
# 3. Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')
```
## iv)Image Reflection
```
# 4. Reflection (Flip)
reflected_image = cv2.flip(image_rgb, 1)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')
```
## v)Image Rotation
```
# 5. Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')
```
## vi)Image Cropping
```
# 6. Cropping
cropped_image = image_rgb[50:300, 100:400]
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
## OUTPUT
## Original image
![download](https://github.com/user-attachments/assets/15c8ef55-9b31-4196-9972-bb453f617345)

## i)Image Translation
![download](https://github.com/user-attachments/assets/44dc2051-e51f-47ed-93c5-64f5deedcbf6)


## ii) Image Scaling
![download](https://github.com/user-attachments/assets/e7b4f8e4-6eec-407b-9079-5fb03678aa21)



## iii)Image shearing
![download](https://github.com/user-attachments/assets/fe6ff7e0-8b32-42a3-af6d-136c02c7dc8e)



## iv)Image Reflection
![download](https://github.com/user-attachments/assets/c76b0a1c-2fb2-44aa-b629-908593c4c853)




## v)Image Rotation
![download](https://github.com/user-attachments/assets/e869ef9c-2f38-4c5b-ab06-a48ebefb70c4)




## vi)Image Cropping
![download](https://github.com/user-attachments/assets/5f72829c-3be5-4c6b-8c2d-5fc416c21f71)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
