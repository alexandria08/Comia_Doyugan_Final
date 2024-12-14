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
  - `Tracking the ball's movement across frames.`
  - `Ball's appearance can change due to lighting or background.`

- **Significance:**
  - `Enables applications like sports analytics and automated refereeing.`
  - `Facilitates tracking in dynamic environments, aiding robotics, and video analysis.`

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
  
## Conclusion
## Additional Materials
