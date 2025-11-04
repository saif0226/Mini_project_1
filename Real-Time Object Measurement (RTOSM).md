**Real-Time Object Measurement (RTOSM)**

A Python application for real-time, non-contact dimension measurement of objects using a standard webcam and computer vision (OpenCV). It overlays the calculated dimensions (width and height in centimeters) directly onto the live video feed.



**Features**

Live Measurement: Dimensions calculated instantly from a webcam feed.



Computer Vision Pipeline: Uses blurring, Canny edge detection, dilation, and contour finding for reliable object detection.



Metric Output: Converts pixel dimensions to centimeters based on a single-point calibration.



Standalone GUI: Simple user interface built with tkinter.



**Tech \& Setup**

Technology	Purpose

Python 3.x	Core language

OpenCV (cv2)	Image processing \& object detection

Tkinter	Graphical User Interface (GUI)

Pillow	Integrating OpenCV frames into Tkinter

Installation

Clone the repository: git clone https://github.com/YourUsername/RTOSM.git



Install dependencies: pip install opencv-python numpy Pillow



Run the app: python RTOSM\_CODE.py



**Calibration Guide**

Accurate measurement requires calibration for your camera's distance and resolution.



Known Object: Place an object with a known width (e.g., a credit card, 8.5 cm) at the distance you plan to measure objects.



Terminal Output: Run the script and check the terminal for the calculated pixels\_per\_cm factor:



\[Calibration] Width in pixels: 323 → pixels\_per\_cm = 38.00

Update Code: Edit line 18 in RTOSM\_CODE.py with the calculated value (e.g., pixels\_per\_cm = 38).



Rerun: Measurements should now be accurate in centimeters.



Note: Calibration is only valid for objects placed at the same distance from the camera.





