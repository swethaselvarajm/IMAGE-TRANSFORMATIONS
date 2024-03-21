# IMAGE-TRANSFORMATIONS

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the necessary libraries and read the original image and save it as a image variable.

## Step2:
Translate the image using a function warpPerpective()

## Step3:
Scale the image by multiplying the rows and columns with a float value.

## Step4:
Shear the image in both the rows and columns.

## Step5:
Find the reflection of the image.

## Step 6:
Rotate the image using angle function.

## Program:
## Developed By: SWETHA S
## Register Number: 212222230155

## i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("img.jpeg")
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

## ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("img.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
## iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("img.jpeg")
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
## iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("img.jpeg")
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
## v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("img.jpeg")
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

## vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("img.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:

### i)Image Translation

![Screenshot 2024-03-21 232745](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/c8c8fc48-9e71-474e-87ca-1eda0fab343e)

### ii) Image Scaling

![Screenshot 2024-03-21 232918](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/577da368-c935-497c-8858-d88791c98ad7)

### iii)Image shearing

![Screenshot 2024-03-21 233136](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/2906fec0-9e3b-4aab-8ccf-472416d915e6)

![Screenshot 2024-03-21 233144](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/ea3b2644-658a-4537-9a62-e835b62c91f9)

### iv)Image Reflection

![Screenshot 2024-03-21 233249](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/831795a3-64bc-48cc-9b86-3df194b5bd1c)

### v)Image Rotation

![Screenshot 2024-03-21 233354](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/6f08d6eb-6411-45c3-bfd6-a3fb6df281fb)

### vi)Image Cropping

![Screenshot 2024-03-21 233455](https://github.com/swethaselvarajm/IMAGE-TRANSFORMATIONS/assets/119525603/9b552e90-5565-4437-87ba-1b7475a2332a)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
