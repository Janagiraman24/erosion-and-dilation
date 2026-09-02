# Implementation of Erosion and Dilation Using OpenCV

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

## Program :
```python
# Step 1: Import required libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

```
```python
# Step 2: Create a blank image using NumPy
image = np.zeros((300, 600), dtype=np.uint8)

```
```python
# Step 3: Insert text onto the image
cv2.putText(
    image,
    'IMAGE PROCESSING',
    (50, 170),
    cv2.FONT_HERSHEY_SIMPLEX,
    2,
    255,
    5,
    cv2.LINE_AA
)
```
```python
# Step 4: Display the original image
plt.figure(figsize=(10, 4))
plt.imshow(image, cmap='gray')
plt.title('Original Image')
plt.axis('off')
plt.show()

```
```python
# Step 5: Create a structuring element (kernel)
kernel = np.ones((5, 5), np.uint8)
print(kernel)

```
```python
# Step 6: Image Erosion
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.figure(figsize=(10, 4))
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')
plt.show()

```
```python
# Step 7: Image Dilation
dilated_image = cv2.dilate(image, kernel, iterations=1)

plt.figure(figsize=(10, 4))
plt.imshow(dilated_image, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')
plt.show()

```
```python
# Step 8: Compare Original, Eroded and Dilated images
plt.figure(figsize=(15, 5))

plt.subplot(1, 3, 1)
plt.imshow(image, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(dilated_image, cmap='gray')
plt.title('Dilated Image')
plt.axis('off')

plt.tight_layout()
plt.show()
```

## Developed By

**Name:** JANAGIRAMAN M

**Register No:** 212224230101

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

<img width="745" height="402" alt="image" src="https://github.com/user-attachments/assets/9bc7f3b5-bd2d-4017-8f7e-bb820d14dca2" />


### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

<img width="727" height="400" alt="image" src="https://github.com/user-attachments/assets/953884be-4efa-466b-b70e-e88bf6a67821" />


### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

<img width="780" height="393" alt="image" src="https://github.com/user-attachments/assets/c1935b67-665f-4b64-8b94-29d2c868db70" />

<img width="1242" height="241" alt="image" src="https://github.com/user-attachments/assets/00dc505b-7df2-4a5b-a350-5fd4051813a1" />



## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
