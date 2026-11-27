# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING:

## Aim:

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

## The program performs the following operations:

* Morphological Opening
* Morphological Closing
* Software Used
* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm:

## Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:

Create or load an input image containing foreground objects.

## Step 3:

Display the original image.

## Step 4:

Create a structuring element (kernel) of suitable size.

## Step 5: Opening Operation:

* Apply the Opening operation using the structuring element.
* Opening consists of Erosion followed by Dilation.
* Remove small foreground noises while preserving the shape of larger objects.
* Display the opened image.

## Step 6: Closing Operation:

* Apply the Closing operation using the structuring element.
* Closing consists of Dilation followed by Erosion.
* Fill small holes and gaps within foreground objects.
* Display the closed image.

## Step 7:

Compare the original, opened, and closed images.


## Program:

## Developed by: SAI PRAVEEN C

## Register Number: 212225230239

### Original Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'SAI PRAVEEN C', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

```
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image with Text")
plt.axis('off')
```

### Opening Operation:

```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB)) 
plt.title("Opening Operation")
plt.axis('off')
```

### Closing Operation:

```
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(closing, cv2.COLOR_BGR2RGB))
plt.title("Closing")
plt.axis("off")
```

## OUTPUT:

## Original Image:

* The input image is displayed.
* The image serves as the source for morphological processing.

## Input Text With Image:

<img width="451" height="454" alt="image" src="https://github.com/user-attachments/assets/0194310c-fa2d-403e-ba72-820f0be07ac8" />

## Opening Operation:

* Original image is displayed.
* Opened image is displayed.
* Small foreground noise is removed.
* Thin protrusions and isolated pixels are eliminated.
* Object boundaries become smoother.

## Output:

<img width="458" height="458" alt="image" src="https://github.com/user-attachments/assets/ca5ac714-4191-40da-ab7f-e8ace3d0a71d" />

## Closing Operation:

* Original image is displayed.
* Closed image is displayed.
* Small holes and gaps inside objects are filled.
* Broken regions are connected.
* Object boundaries become more continuous.

## Output:

<img width="454" height="462" alt="image" src="https://github.com/user-attachments/assets/a50b431e-b79f-4fb0-8550-9214db752714" />

## Applications:

## Opening:

* Noise removal in binary images.
* Separation of connected objects.
* Preprocessing for object detection.

## Closing:

* Filling small holes in objects.
* Connecting nearby components.
* Enhancing segmented regions.

## Advantages:

## Opening:

* Removes unwanted foreground noise.
* Preserves major object structures.
* Improves segmentation quality.

## Closing:

* Restores object continuity.
* Eliminates small background gaps.
* Improves object representation.

## Result:

Thus, the morphological operations Opening and Closing are successfully implemented using OpenCV.
