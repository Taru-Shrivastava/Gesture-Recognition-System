# Gesture-Recognition-System
 
This Python script implements a gesture recognition system that controls video playback and volume based on hand gestures using OpenCV and MediaPipe. The system captures live video from the camera and processes hand landmarks to detect the number of raised fingers. These gestures are mapped to specific video control functions.

Camera Initialization and Setup:

The script starts by initializing the camera and setting a high resolution (2000x2000). The video stream is captured, flipped horizontally for a mirror effect, and processed frame by frame.
Hand Detection:

The handobj from MediaPipe is used to process each frame and detect hand landmarks. If a hand is detected, the script calculates the number of raised fingers by analyzing the landmark positions.
Gesture Mapping to Controls:

Different numbers of raised fingers are mapped to specific video control actions:
1 finger: Play or pause the video.
2 fingers: Fast forward the video by 20 seconds.
3 fingers: Rewind the video by 20 seconds.
4 fingers: Decrease the volume by 30 units.
6 fingers: Increase the volume by 30 units.
These actions are triggered if the gesture remains consistent for at least 0.2 seconds to avoid accidental commands.
Hand Landmark Visualization:

The system also draws the hand landmarks and connections on the video feed using OpenCV.
Performance Monitoring:

The script calculates and displays the frames per second (FPS) to monitor real-time performance.
Video Display:

The processed video frames with annotations are displayed in a window, and the system waits for 2 milliseconds before reading the next frame, enabling a continuous loop for real-time gesture recognition.
