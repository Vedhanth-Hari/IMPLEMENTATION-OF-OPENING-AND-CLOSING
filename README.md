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

### DEVELOPED BY: VEDHANTH H
### REGISTER NO: 212224240181


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
cv2.putText(img, 'VEDHANTH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
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

<img width="611" height="100" alt="image" src="https://github.com/user-attachments/assets/fe5b2f4a-7e15-4988-9597-f5a3a14db8d8" />


### Display the result of Opening:
<img width="608" height="110" alt="image" src="https://github.com/user-attachments/assets/ca02e2e2-89c1-4615-b0aa-d189c9e81966" />



### Display the result of Closing:

<img width="613" height="110" alt="image" src="https://github.com/user-attachments/assets/b5785bdf-5b03-41a3-91c0-21fa9b814e77" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
