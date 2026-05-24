# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image
 
## Program:
### Dinesh Karthik R
### 212224230068
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
# Create a blank image
image = np.zeros((500, 600, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'kishore', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Erode the image


# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Dilate the image
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="961" height="577" alt="image" src="https://github.com/user-attachments/assets/43d8fd72-b8c0-45de-bf30-c0d7ec57f76f" />


### Display the Eroded Image
<img width="917" height="571" alt="image" src="https://github.com/user-attachments/assets/0cf2a56f-c5ca-43ed-8eee-e39b5844a29a" />


### Display the Dilated Image
<img width="1092" height="567" alt="image" src="https://github.com/user-attachments/assets/d25b9a65-c2d3-4b83-b361-70207c98617f" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
