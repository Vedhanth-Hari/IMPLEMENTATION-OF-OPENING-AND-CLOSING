# IMPLEMENTATION-OF-OPENING-AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1.Anaconda - Python 3.7

2.OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

## Program:

### DEVELOPED BY: KATHI HASINI
### REGISTER NO: 212224240074


### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'MOUNIKA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
#### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```


## Output:
### Display the input Image:
<img width="614" height="111" alt="image" src="https://github.com/user-attachments/assets/0211a795-ed6e-4e11-abd2-e13b54fce062" />


### Display the result of Opening:
<img width="614" height="105" alt="image" src="https://github.com/user-attachments/assets/0e017c97-afb1-4626-89fd-c8158d2fd359" />


### Display the result of Closing:
<img width="613" height="104" alt="image" src="https://github.com/user-attachments/assets/79b95059-117e-4900-8bde-d2cba411a419" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
