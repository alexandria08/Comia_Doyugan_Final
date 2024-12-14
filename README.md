# MeXE402_Finals_Alexandria-Comia_Tristan-Kiefer-Doyugan

<div align="center">
 
# **Tracking a Basketball in a Video**

![bball header](https://github.com/user-attachments/assets/778cb0fb-87da-44e8-a027-e48db049c1bd)

</div>

## I. Introduction🏀
<div align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Welcome to the basketball tracking project! This repository demonstrates how to track a basketball in a video using computer vision techniques such as HSV color detection and object tracking. The goal is to accurately follow the ball's movement in various scenarios, useful for sports analysis, automated refereeing, and motion tracking systems.
</div>

- **Problem:**
  - Tracking a ball in a video using HSV (Hue, Saturation, Value) addresses the problem of object detection and tracking in dynamic environments, a core challenge in computer vision. By leveraging color segmentation, HSV tracking isolates the ball based on its unique color properties, making it robust against varying lighting conditions. 

- **Significance:**
  - Tracking a ball using HSV in video facilitates applications like sports analytics, enabling real-time performance evaluation and automated refereeing for improved accuracy. It also aids robotics and video analysis by enhancing object tracking in dynamic environments, crucial for motion prediction and automation.

## II. Abstract🏀
- **Objective:** Track a basketball in a video using HSV color space for object detection and motion tracking.
  
- **Approach:** Involves converting video frames to HSV color space for effective ball detection, applying color thresholds to isolate the basketball, and using contour detection to track its movement.
  
- **Expected Results:** Accurate and real-time tracking of the basketball.
## III. Project Methods🏀
- **Cloning Repository:** The project repository is cloned to access video and code files.

- **Video Input:** A video file is opened using cv2.VideoCapture.

- **HSV Conversion:** Each frame is converted to HSV to isolate the basketball color.

- **Color Masking:** A mask is created to highlight the basketball using specific HSV value ranges.

- **Contour Detection:** Contours are found from the masked image to detect the ball.

- **Tracking:** The ball's center is determined and tracked across frames.

- **Drawing Trajectory:** The ball's path is drawn using lines.

- **Output Video:** The processed frames are saved in a new video file.
  
## IV. Conclusion🏀
- **Findings:**
  - `The code effectively tracks a basketball by detecting its color in the HSV color.`

- **Challenges:**
  - `Handling varying lighting conditions and ensuring stable tracking when the ball is partially obscured or moving fast.`

- **Outcomes:**
  - `Successful tracking of the ball across frames, with a continuous path drawn. The video is saved with the tracked trajectory, providing a visual representation of the ball's movement.`
    
## V. Additional Materials🏀

<div align="center">
 
### **Basketball Dataset**

[![Video Thumbnail](https://img.youtube.com/vi/mdobMUUWSLQ/0.jpg)](https://www.youtube.com/watch?v=mdobMUUWSLQ)


_Click on the image above to watch the video._


</div>

<br>

<div align="center">
 
### **Tracked Basketball**

[![Watch the video](https://img.youtube.com/vi/m3v4pw8J-Yo/0.jpg)](https://www.youtube.com/watch?v=m3v4pw8J-Yo)


_Click on the image above to watch the video._


</div>

<br>

## Cloning the Repository

```bash
!git clone https://github.com/alexandria08/Comia_Doyugan_Final.git
%cd opencvTutorial/
from IPython.display import clear_output
clear_output()
```
## Code for Ball Tracking Using HSV

```python
import cv2
import numpy as np
from google.colab.patches import cv2_imshow

ball = []
cap = cv2.VideoCapture("/content/Comia_Final/Ball Tracking.mov")
out = cv2.VideoWriter('tracked ball.avi', cv2.VideoWriter_fourcc('M', 'J', 'P', 'G'), 10, (1920, 1080))
while cap.isOpened():
    ret, frame = cap.read()
    if not ret:
        break
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
    lower_hue = np.array([10, 100, 100])
    upper_hue = np.array([25, 255, 255])
    mask = cv2.inRange(hsv, lower_hue, upper_hue)

    (contours, _) = cv2.findContours(mask, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)
    center = None

    if len(contours) > 0:
        c = max(contours, key=cv2.contourArea)
        ((x, y), radius) = cv2.minEnclosingCircle(c)
        M = cv2.moments(c)
        try:
            center = (int(M["m10"] / M["m00"]), int(M["m01"] / M["m00"]))
            cv2.circle(frame, center, 10, (255, 0, 0), -1)
            ball.append(center)
        except:
            pass
        if len(ball) > 2:
            for i in range(1, len(ball)):
                cv2.line(frame, ball[i - 1], ball[i], (0, 0, 255), 5)
    out.write(frame)
out.release()
```

## VI. References🏀
1. Adobe Stock. (n.d.). Free throw basketball animation video sport activity equipment motion graphic design. Retrieved December 14, 2024, from https://stock.adobe.com/ph/video/free-throw-basketball-animation-video-sport-activity-equipment-motion-graphic-design/750453084
2. OpenCV Tutorial - Easy run on Colab with Code (2021). Tracking basketball movement with HSV and OpenCV [Video]. YouTube. Retrieved December 14, 2024, from https://www.youtube.com/watch?v=E3Lg4aZVCAU

