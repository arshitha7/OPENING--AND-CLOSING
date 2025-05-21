# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Load the input image using cv2.imread().

### Step2:
<br>
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().


### Step3:
<br>
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.


### Step4:
<br>
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.


### Step5:
<br>
Use plt.subplot() to show the original, opening, and closing images side by side.


 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"SaVeEtHa",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/67432ddb-f6a3-4cc5-9775-0695c7f1dd59)


### Display the result of Opening
![image](https://github.com/user-attachments/assets/4f7c4835-081a-442a-bdf3-cbd522721fdb)

### Display the result of Closing
![image](https://github.com/user-attachments/assets/831a1c21-72c4-422c-80b9-c8c21230a137)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
