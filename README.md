# OpenCV Opening and Closing Operations

## Overview
This project demonstrates morphological opening and closing operations using Python and OpenCV. These operations are commonly used in image preprocessing for noise removal, gap filling, object smoothing, and shape enhancement in computer vision applications.

---

## Features

- Load and display an input image
- Convert image to grayscale
- Apply Binary Thresholding
- Perform Morphological Opening
- Perform Morphological Closing
- Remove noise from images
- Fill small holes and gaps in objects
- Display processed outputs using Matplotlib

---

## Technologies Used

- Python 3.7+
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- Jupyter Notebook / VS Code

---

## Morphological Operations

### Opening Operation
Opening is performed by applying erosion followed by dilation. It removes small noises and separates connected objects.

### Closing Operation
Closing is performed by applying dilation followed by erosion. It fills small holes and connects nearby objects.

### Structuring Element (Kernel)
A kernel matrix is used to process neighboring pixels during morphological transformations.

---

## Algorithm

1. Import required libraries
2. Read the input image using OpenCV
3. Convert the image to grayscale
4. Apply Binary Thresholding
5. Create a structuring element (kernel)
6. Perform Opening operation
7. Perform Closing operation
8. Display all outputs using Matplotlib
9. Compare processed results

---
## Applications

- Image Preprocessing
- Noise Removal
- Object Enhancement
- Medical Image Processing
- OCR Systems
- Computer Vision Applications

---
### PROGRAMM & OUTPUT:
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Jude Clement Jose G', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
<img width="705" height="955" alt="image" src="https://github.com/user-attachments/assets/29602ec7-9e49-4656-98c8-bbf8b0dedbfb" />

```python
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
<img width="555" height="509" alt="image" src="https://github.com/user-attachments/assets/9eaa0043-4efb-409c-92cf-e7a8b65d5c8f" />

```python
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
<img width="507" height="494" alt="image" src="https://github.com/user-attachments/assets/139a245b-6d3a-495b-b93e-bd04b4af6001" />

```python
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Display the result of Closing
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))
plt.title("Closing Operation")
plt.axis('off')
plt.show()
```
<img width="555" height="511" alt="image" src="https://github.com/user-attachments/assets/ada8d065-d0e5-4e6a-874d-eade26254373" />

## Result

The implementation successfully demonstrates opening and closing morphological operations using OpenCV. These techniques improve image quality by removing noise, smoothing object boundaries, and filling unwanted gaps in images.

---
