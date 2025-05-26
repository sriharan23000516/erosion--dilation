# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1: Import the neccesary packages
### Step2: Creat the text using cv2.put Text

### Step3: Create the structuting element

### Step4: Erodde the image

### Step5: Dilate the image
 
## Program:
### Name: SARISH VARSHAN V
### Register Number: 212223230196
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='FRANK', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)

kernal = np.ones((5,5),dtype=np.uint8)

img1 = cv2.erode(img,kernal,iterations = 2)
display_img(img1,"Eroded Image")

dilate = cv2.dilate(img,kernal,iterations = 3)
display_img(dilate,"Dilated Image")
```
## Output:
### Display the input Image
![Screenshot 2025-05-20 210017](https://github.com/user-attachments/assets/efe27ef1-a135-4423-bb84-1e4fa2ca8b96)


### Display the Eroded Image

![Screenshot 2025-05-20 210025](https://github.com/user-attachments/assets/44df0f19-db1e-491c-9210-533c018de156)


### Display the Dilated Image

![Screenshot 2025-05-20 210035](https://github.com/user-attachments/assets/37a93c4f-2cc2-4986-85af-966ac84b45fb)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
