
# **Hand Tracking Volume Controller**







This project is a real-time volume control application using hand gestures and computer vision. By tracking hand landmarks through a webcam, the program allows the user to adjust their system volume by changing the distance between their thumb and index finger. It is built with OpenCV for image processing, Mediapipe for hand tracking, and Pycaw for controlling system audio.



## **_Features_**

Real-time Hand Tracking: Detects and tracks hand landmarks using Mediapipe.
Volume Control: Adjusts system volume based on the distance between the thumb and index finger.
Smoothing Mechanism: Smoothens the volume changes for a more controlled experience.
Visual Feedback: Displays a volume bar and current volume level on the screen.


### **_Prerequisites To run this project, you'll need:_**







Python 3.7+
Webcam (or any other camera device)
Installation
Clone the repository:

Bash
Copy code
git clone https://github.com/yourusername/HandTrackingVolumeControl.git
cd HandTracking_VolumeControl

Install dependencies: Install the necessary packages using the following command:



    pip install opencv-python mediapipe pycaw comtypes numpy
 Add the HandTrackingModule.py file:
 
Ensure HandTrackingModule.py is in the project directory. This module handles hand detection and provides methods to detect landmarks, calculate distances, and track specific finger positions.




*  Project Structure
*  Prerequisites




 



2. [ ] ├── HandTrackingModule.py                
3. [ ] ├── VolumeHandController.py     

# Project documentation


Usage
Run the Program:



Place your hand in front of the webcam.
Change the distance between your thumb and index finger to adjust the volume:
Increase Volume: Move thumb and index finger further apart.
Decrease Volume: Bring thumb and index finger closer.
The pinky finger can be used as a control lock. When raised, it prevents any volume change.
Exit: Press q to quit the application.

**_Code Explanation Hand Detection:_**

The HandTrackingModule.py uses Mediapipe to detect and track hand landmarks.

**_Volume Control:_** The application calculates the distance between the thumb and index finger landmarks to map this distance to the system volume range using Pycaw.

Smoothing Mechanism: To make volume adjustments smoother, volume values are rounded and updated at intervals. A smoothing factor is applied to ensure minor finger movements don't result in abrupt volume changes.

**_Troubleshooting IndexError:_**

 Ensure the bounding box coordinates (bbox) are valid by checking for the presence of detected landmarks.
Camera Issues: Make sure your camera is connected and functional.
Audio Issues: Pycaw works only on Windows systems, so this project is currently Windows-only.
Acknowledgements
Mediapipe: For hand-tracking and landmark detection.
Pycaw: For controlling system audio on Windows.
OpenCV: For real-time image processing and visualization.