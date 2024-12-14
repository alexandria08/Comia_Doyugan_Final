# MeXE402_Finals_Alexandria-Comia_Tristan-Kiefer-Doyugan

<div align="center">
 
# **Tracking a Basketball in a Video**

![bball header](https://github.com/user-attachments/assets/778cb0fb-87da-44e8-a027-e48db049c1bd)

</div>

## Introduction🏀
<div align="justify">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Welcome to the basketball tracking project! This repository demonstrates how to track a basketball in a video using computer vision techniques such as HSV color detection and object tracking. The goal is to accurately follow the ball's movement in various scenarios, useful for sports analysis, automated refereeing, and motion tracking systems.
</div>

- **Problem:**
  - Tracking a ball in a video using HSV (Hue, Saturation, Value) addresses the problem of object detection and tracking in dynamic environments, a core challenge in computer vision. By leveraging color segmentation, HSV tracking isolates the ball based on its unique color properties, making it robust against varying lighting conditions. 

- **Significance:**
  - Tracking a ball using HSV in video facilitates applications like sports analytics, enabling real-time performance evaluation and automated refereeing for improved accuracy. It also aids robotics and video analysis by enhancing object tracking in dynamic environments, crucial for motion prediction and automation.

## Abstract🏀
- **Objective:** Track a basketball in a video using HSV color space for object detection and motion tracking.
  
- **Approach:** Involves converting video frames to HSV color space for effective ball detection, applying color thresholds to isolate the basketball, and using contour detection to track its movement.
  
- **Expected Results:** Accurate and real-time tracking of the basketball.
## Project Methods🏀
- **Cloning Repository:** The project repository is cloned to access video and code files.

- **Video Input:** A video file is opened using cv2.VideoCapture.

- **HSV Conversion:** Each frame is converted to HSV to isolate the basketball color.

- **Color Masking:** A mask is created to highlight the basketball using specific HSV value ranges.

- **Contour Detection:** Contours are found from the masked image to detect the ball.

- **Tracking:** The ball's center is determined and tracked across frames.

- **Drawing Trajectory:** The ball's path is drawn using lines.

- **Output Video:** The processed frames are saved in a new video file.
  
## Conclusion🏀
- **Findings:**
  - `The code effectively tracks a basketball by detecting its color in the HSV color.`

- **Challenges:**
  - `Handling varying lighting conditions and ensuring stable tracking when the ball is partially obscured or moving fast.`

- **Outcomes:**
  - `Successful tracking of the ball across frames, with a continuous path drawn. The video is saved with the tracked trajectory, providing a visual representation of the ball's movement.`
    
## Additional Materials🏀

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


## References🏀
1. Adobe Stock. (n.d.). Free throw basketball animation video sport activity equipment motion graphic design. Retrieved December 14, 2024, from https://stock.adobe.com/ph/video/free-throw-basketball-animation-video-sport-activity-equipment-motion-graphic-design/750453084
