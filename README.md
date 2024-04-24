## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: KEERTHANA S
REG.NO: 212222230066
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Narmadha',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image
![pic-1](https://github.com/Keerthanasampathkumar/erosion--dilation/assets/119477890/5521c190-7418-40c2-8b1e-1b27ccca44e0)


#### Display the Eroded Image
![pic-2](https://github.com/Keerthanasampathkumar/erosion--dilation/assets/119477890/ad2f2abe-2352-4113-a7ad-e0d621dcd8cc)


#### Display the Dilated Image
![pic-3](https://github.com/Keerthanasampathkumar/erosion--dilation/assets/119477890/8df58bed-2c14-418f-8ba1-be7c266a7427)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
