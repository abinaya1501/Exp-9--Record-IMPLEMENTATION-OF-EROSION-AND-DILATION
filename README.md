# Implementation of Erosion and Dilation Using OpenCV
# NAME: ABINAYA A

# REG NO: 212224230004

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

**Name:** ABINAYA A

**Register No:** 212224230004

## PROGRAM

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Create a blank black image
img = np.zeros((200, 600), dtype=np.uint8)

# Step 3: Insert white text on the image
cv2.putText(img, "Abinaya A", (30, 140), cv2.FONT_HERSHEY_SIMPLEX,
            3, 255, 5, cv2.LINE_AA)

# Step 4: Display the original image
plt.figure(figsize=(8, 4))
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.show()
```
### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((200, 600), dtype=np.uint8)
cv2.putText(img, "Abinaya A", (30, 140), cv2.FONT_HERSHEY_SIMPLEX,
            3, 255, 5, cv2.LINE_AA)

# Step 5: Structuring element (kernel)
kernel = np.ones((5, 5), np.uint8)

# Step 6: Erosion shrinks the white text inward
eroded = cv2.erode(img, kernel, iterations=1)

plt.figure(figsize=(12, 4))
plt.subplot(1, 2, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(eroded, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")
plt.show()
```
### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((200, 600), dtype=np.uint8)
cv2.putText(img, "Abinaya A", (30, 140), cv2.FONT_HERSHEY_SIMPLEX,
            3, 255, 5, cv2.LINE_AA)

# Same kernel as erosion
kernel = np.ones((5, 5), np.uint8)

# Step 7: Dilation expands the white text outward
dilated = cv2.dilate(img, kernel, iterations=1)

plt.figure(figsize=(12, 4))
plt.subplot(1, 2, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(dilated, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")
plt.show()
```
## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="457" height="467" alt="image" src="https://github.com/user-attachments/assets/a21e6efc-7a65-47cf-bae9-7af6d80e7ebe" />



### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

<img width="450" height="467" alt="image" src="https://github.com/user-attachments/assets/8f493cfa-df1e-461b-a924-9d06a8067673" />




### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="448" height="466" alt="image" src="https://github.com/user-attachments/assets/a3c495d8-8157-4eb5-a172-7d40ef40e259" />




## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
