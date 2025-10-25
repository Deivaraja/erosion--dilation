# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>


### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

 
## Program:


# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'JANARTHANAN K', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```
# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
<br>
<br>
<img width="908" height="118" alt="image" src="https://github.com/user-attachments/assets/b1d21a69-25d1-4063-b14c-601fa5396ea0" />

<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>
<img width="852" height="180" alt="image" src="https://github.com/user-attachments/assets/f8131df3-bee3-4108-8a65-fed24a92a92a" />


<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<img width="981" height="171" alt="image" src="https://github.com/user-attachments/assets/7f995f1a-1807-4432-9a8c-34e194605ab1" />

<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
