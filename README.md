# EX. No: 6 – EDGE DETECTION
### Developed By : VIMALRAJ B
### Register Number : 212224230304
### Aim :
To implement various edge detection techniques using Python and OpenCV to identify and highlight the edges and boundaries of objects in an image.
### Requirements :
Hardware Requirements:
- Computer or Laptop
- Minimum 4 GB RAM
Software Requirements:
- Python
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib
### Procedure :
1. Import the required libraries such as OpenCV, NumPy, and Matplotlib.
2. Read the input image using cv2.imread().
3. Convert the original image into grayscale using cv2.cvtColor().
4. Display the original image using Matplotlib.
5. Apply the Sobel Edge Detection method in X and Y directions.
6. Combine both Sobel directions using cv2.magnitude().
7. Apply the Laplacian Edge Detection method to identify rapid intensity changes.
8. Apply the Canny Edge Detection method using threshold values 50 and 150.
9. Display the detected edges using Matplotlib.

### Program : 
### Step 1: Import Libraries and Load the Image
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('ex.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('on')
```
### Step 2: Sobel Edge Detection
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('on')
```
### Step 3: Laplacian Edge Detection
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('on')
```
### Step 4: Canny Edge Detection
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('on')
```

### Output : 
### Step 1: Original Image
<img width="516" height="576" alt="image" src="https://github.com/user-attachments/assets/eab59efb-65b8-4608-81af-7b457f7a17bf" /></br>
### Step 2: Sobel Edge Detection
<img width="528" height="574" alt="image" src="https://github.com/user-attachments/assets/9c70fbed-7c65-4b26-afc2-f1b274a0e877" /></br>
### Step 3: Laplacian Edge Detection
<img width="535" height="580" alt="image" src="https://github.com/user-attachments/assets/b11b393c-197a-40c3-82c0-983adb445c32" /></br>
### Step 4: Canny Edge Detection
<img width="526" height="592" alt="image" src="https://github.com/user-attachments/assets/70ea6e84-41a2-4f23-aebf-62de6fcc57a2" /></br>



















### Result :
Thus, various edge detection techniques such as Sobel, Laplacian, and Canny were successfully implemented using Python and OpenCV. The edges and boundaries of objects in the input image were identified and displayed successfully.
