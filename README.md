# WORKSHOP-3-Canny-Edge-Detection
# Developed By
# Name: Sairam K
# Reg No: 212225240132
## Aim

To detect edges in an image using the Canny Edge Detection technique.

## Requirements

- Anaconda
- Jupyter Notebook
- OpenCV
- Matplotlib
- Input Image

## Steps

1. Open Jupyter Notebook using Anaconda.
2. Read the input image using OpenCV.
3. Convert the image to grayscale.
4. Apply Gaussian Blur to reduce noise.
5. Apply the Canny Edge Detection algorithm.
6. Display the original image and the detected edges.

## Algorithm

```text
Input Image
     ↓
Convert to Grayscale
     ↓
Gaussian Blur
     ↓
Canny Edge Detection
     ↓
Display Original Image
     ↓
Display Detected Edges
```
## Program
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('me.jpg', cv2.IMREAD_GRAYSCALE)

blurred = cv2.GaussianBlur(img, (5,5), 0)

edges = cv2.Canny(blurred, 50, 150)

plt.figure(figsize=(10,5))

plt.subplot(121)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title('Detected Edges')
plt.axis('off')

plt.show()
```

## Output
<img width="612" height="283" alt="image" src="https://github.com/user-attachments/assets/e8292780-ecb8-4bd9-be69-e707788c5eed" />

