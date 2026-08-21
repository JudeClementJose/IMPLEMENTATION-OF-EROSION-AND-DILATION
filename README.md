# OpenCV Erosion and Dilation

This project demonstrates morphological image processing techniques using Python and OpenCV. Erosion and dilation are fundamental operations used for noise removal, shape enhancement, object extraction, and preprocessing in computer vision applications.

---

## Features

- Load and display an input image
- Convert image to grayscale
- Apply Binary Thresholding
- Perform Erosion Operation
- Perform Dilation Operation
- Compare original and processed outputs
- Visualize morphological transformations using Matplotlib

---

## Technologies Used

- Python 3.7+
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Jupyter Notebook / VS Code

---

## Morphological Operations

### Erosion
Erosion removes small white noises and shrinks foreground objects in a binary image.

### Dilation
Dilation expands foreground regions, fills gaps, and enhances object boundaries.

### Structuring Element (Kernel)
A kernel matrix is used to determine how neighboring pixels affect the morphological operation.

---

## Algorithm

1. Import required libraries
2. Read the input image using OpenCV
3. Convert the image to grayscale
4. Apply Binary Thresholding
5. Create a structuring element (kernel)
6. Perform erosion using OpenCV
7. Perform dilation using OpenCV
8. Display processed outputs using Matplotlib
9. Compare morphological operation results

---



## Applications

- Image Preprocessing
- Noise Removal
- Shape Analysis
- Object Detection
- Medical Imaging
- Computer Vision Systems

---
---


## PROGRAMM & OUTPUT:
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HELLO Jude', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
<img width="737" height="953" alt="image" src="https://github.com/user-attachments/assets/e6a791b0-275f-4e4c-b290-b5b9d6abe6c5" />

```python
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
<img width="464" height="466" alt="image" src="https://github.com/user-attachments/assets/6a366781-8032-4a0f-b67c-7b79cc700e95" />

```python
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
<img width="493" height="464" alt="image" src="https://github.com/user-attachments/assets/2c15de83-0b60-41a5-949b-22672f54fc39" />

```python
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
<img width="449" height="458" alt="image" src="https://github.com/user-attachments/assets/16a9e351-7c6b-4b48-97c5-e833b070ebc5" />


## Result

The implementation successfully demonstrates erosion and dilation operations using OpenCV. These morphological techniques help improve image quality, remove unwanted noise, and enhance object structures for computer vision tasks.

