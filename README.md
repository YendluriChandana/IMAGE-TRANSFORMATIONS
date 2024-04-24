`# IMAGE-TRANSFORMATIONS


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
# Developed By: Yendluri Chandana
# Register Number: 212223100063
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
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/4a7613bd-226c-42d4-8422-310be87c6a89)


### ii) Image Scaling
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/b86e03bf-0c67-4cfe-9f10-8e2ea093559d)

![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/8e15361d-3383-4474-b4c3-709a5ce576fb)


### iii)Image shearing
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/0b7b5eab-4e4d-45c6-8273-14b244fa184d)

### iv)Image Reflection
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/775758e9-684c-4a30-b67e-c5a9ebc04196)



![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/1f0b1b74-f74f-4028-9e0b-33897a8f46fe)

### v)Image Rotation
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/cd1654aa-3a47-499e-a134-81a5653d1466)



### vi)Image Cropping
![image](https://github.com/YendluriChandana/IMAGE-TRANSFORMATIONS/assets/139842204/f105a3eb-c754-4067-936e-6e969e0a16ff)


## Result: 


Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
