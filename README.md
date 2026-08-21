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
<img width="1168" height="854" alt="image" src="https://github.com/user-attachments/assets/b61ebf1a-7ce6-45f0-aca0-d5c49e842abc" />

```python
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
<img width="1003" height="556" alt="image" src="https://github.com/user-attachments/assets/bef5b17e-eb48-4bac-aab3-0842c39f7829" />

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
<img width="994" height="559" alt="image" src="https://github.com/user-attachments/assets/caa665f4-ecfc-4a2d-81d5-e019bae2f2fb" />

```python
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
<img width="997" height="556" alt="image" src="https://github.com/user-attachments/assets/dc31a6fe-e440-4724-9059-ed95ab3c8ac9" />


## Result

The implementation successfully demonstrates erosion and dilation operations using OpenCV. These morphological techniques help improve image quality, remove unwanted noise, and enhance object structures for computer vision tasks.

