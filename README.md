# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program:

``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'MOUNIKA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<br>
<br>
<br>
<img width="800" height="630" alt="image" src="https://github.com/user-attachments/assets/673730ff-fcc5-4032-9900-51b8bb4b8a33" />

<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>
<img width="972" height="619" alt="image" src="https://github.com/user-attachments/assets/fd7e3c8e-c509-4b09-ba1b-6f695b4007d7" />

<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<img width="821" height="611" alt="image" src="https://github.com/user-attachments/assets/a98d7e23-a565-4748-a24d-e9e899beef27" />

<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
