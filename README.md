# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.



## Program:
```python
# Developed By: Thanjiyappan K
# Register Number: 212222240108
# i)Image Translation
```
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()


# ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))

#iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis
plt.show()

#iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
# v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
# vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
cropped_img=input_image[100:300, 100:300]
plt.imshow(cropped_img)

```
## Output:
### i)Image Translation
![image](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/873e7481-c7bf-47b9-bf15-da7371731634)


### ii) Image Scaling
![Screenshot from 2024-03-11 20-30-22](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/87f8c5d7-ef62-4449-8a41-b1cb965e708d)

![Screenshot from 2024-03-11 20-31-50](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/21eeb3da-ed19-49bf-9062-327579666fa6)


### iii)Image shearing
![image](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/873e7481-c7bf-47b9-bf15-da7371731634)

### iv)Image Reflection
![image](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/b8dbe4a6-7482-425a-876a-861bba074e88)


![Screenshot from 2024-03-11 20-34-14](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/8c80e087-45e9-43e6-9691-74c2795d4c35)

### v)Image Rotation
![Screenshot from 2024-03-11 20-33-25](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/f55fca77-562f-4f57-b026-72b608146626)


### vi)Image Cropping
![Screenshot from 2024-03-11 20-36-30](https://github.com/22009011/IMAGE-TRANSFORMATIONS/assets/118343461/9aea84d3-f04b-4cf2-94fe-9adf42d4f3e1)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
