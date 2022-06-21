### Ex.No:05
### DATE: 
# <p align="center"> Image-Transformation

</p>

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and read the original image.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### Step 6:
Rotate the image.

### Step 7:
Crop the image.

## Program:
```python
Developed By:KUMARAVEL V
Register Number:212220230027  
import cv2
import numpy as np
import matplotlib.pyplot as plt
original_img=cv2.imread("image.jpeg")
original_img=cv2.cvtColor(original_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(original_img)
row,col,dim=original_img.shape

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)

iii)Image Shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)

iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)



```
## Output:
### i)Image Translation
![WhatsApp Image 2022-04-27 at 8 10 46 PM](https://user-images.githubusercontent.com/75235334/165566488-cc622402-04db-40f5-a738-5b3c661ad9b0.jpeg)


### ii) Image Scaling

![WhatsApp Image 2022-04-27 at 8 10 46 PM (1)](https://user-images.githubusercontent.com/75235334/165566433-22b65036-15a9-4e11-8feb-1e74a0d710ed.jpeg)

### iii)Image shearing
![image](https://user-images.githubusercontent.com/75235334/165563061-b2773031-d6df-4be6-953e-f7261e05b195.png)



### iv)Image Reflection
![WhatsApp Image 2022-04-27 at 8 10 46 PM (2)](https://user-images.githubusercontent.com/75235334/165566336-c302349e-07d3-47fa-88c2-bf8fc502311d.jpeg)


### v)Image Rotation


![image](https://user-images.githubusercontent.com/75235334/165563296-948e4425-7000-495d-8ebe-7948f4e0ccaa.png)



### vi)Image Cropping

![image](https://user-images.githubusercontent.com/75235334/165562871-6e95ac34-ee91-4489-adee-c1b20c24068c.png)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
