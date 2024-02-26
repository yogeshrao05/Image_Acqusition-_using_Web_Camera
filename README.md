# Image_Acqusition-_using_Web_Camera
## Aim
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
</br>
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
## Step 1:
Use cv2.VideoCapture(0) to access web camera

## Step 2:
Use cv2.imread to read the video or image

## Step 3:
Use cv2.imwrite to save the image

## Step 4:
Use cv2.imshow to show the video

## Step 5:
End the program and close the output video window by pressing 'q'.
## Program:
``` Python
### Developed By: yogesh rao S D
### Register No:212222110055
```
## i) Write the frame as JPG file
```
import cv2
videoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=videoCaptureObject.read()
    cv2.imwrite("rao.jpg",frame)
    result=False
videoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('rao ',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222110055 yogesh rao',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222110055 yogesh rao',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![Screenshot 2024-02-24 212726](https://github.com/saiganesh2006/Image_Acqusition-_using_Web_Camera/assets/145742342/7780c510-ba5c-45d8-ae2f-83c6f5c8435f)
### ii) Display the video
![Screenshot 2024-02-24 213231](https://github.com/saiganesh2006/Image_Acqusition-_using_Web_Camera/assets/145742342/b9ed251f-9479-4825-9e0c-fb1891e78292)
### iii) Display the video by resizing the window
![Screenshot 2024-02-24 213349](https://github.com/saiganesh2006/Image_Acqusition-_using_Web_Camera/assets/145742342/fb2e8591-67be-420a-8866-a9a72ba8312c)
### iv) Rotate and display the video
![Screenshot 2024-02-24 213529](https://github.com/saiganesh2006/Image_Acqusition-_using_Web_Camera/assets/145742342/d89105a5-96a2-421f-ad7b-7fb310212b4c)
## Result:
Thus the image is accessed from webcamera and displayed using openCV.









