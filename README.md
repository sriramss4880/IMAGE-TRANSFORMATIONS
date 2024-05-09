# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image using angle function.

## Program:
```python
Developed By: SRIRAM S S
Register Number: 212222230150
```

### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("rajini.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/1a05cec5-3bfe-46f8-a926-94b19c5d9276)        
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/c8f75222-12bd-4bc4-beaa-6f95b5c5ec36)        


### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/064b6be9-4ddb-4a96-85cf-ff737ce987dd)          
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/e89e461e-ceda-4add-9a59-ff5f5361f55c)          


### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/a957d6b9-105a-4b89-82bb-c0e378d75ab0)          
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/6095fbea-78a2-4d9b-9bf2-cf06f151da1d)            

### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/d909367f-912f-4528-ba67-cba07ea012b7)          
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/f15e77dc-38bd-4b12-af54-4d7ae981cb3e)        



### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/f5bda604-da34-4955-bff7-361909bab705)
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/054608c5-9e95-4a67-9203-274b5d33b924)



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("rajini.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/4f4c933e-7dc3-42a2-98df-3762e1671889)            
![image](https://github.com/Yogeshvar005/IMAGE-TRANSFORMATIONS/assets/113497367/de6e6255-7074-47d2-b7c3-1ca1439fcd35)              

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
