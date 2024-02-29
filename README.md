# live_stress_DETECTOR
Welcome to this code snippet that demonstrates real-time emotion and stress detection using a webcam! This script utilizes OpenCV and DeepFace libraries to detect faces from the webcam feed, analyze emotions, calculate stress levels based on facial expressions, and overlay the detected emotions and stress on the video feed. Additionally, it provides certain sources to overcome stress.

🔍 Key Components:

Importing Libraries: The code starts by importing the necessary libraries, including OpenCV, matplotlib, and DeepFace.
Webcam Initialization: The script initializes the webcam using OpenCV's VideoCapture class. It tries to use the second camera (index 1) and falls back to the default camera (index 0) if the second camera is unavailable.
Face Detection: OpenCV's Haar Cascade Classifier is employed to detect faces in each frame of the webcam feed. Detected faces are outlined with rectangles.
Emotion and Stress Analysis: DeepFace's analyze function is used to analyze emotions and calculate stress in the detected faces. The enforce_detection parameter is set to False to avoid redundant face detection, as we're already using the Haar Cascade for this purpose.
Overlaying Emotions and Stress: The dominant emotion and stress level detected by the DeepFace analysis are extracted and overlaid as text on the video feed, near the top-left corner of the frame.
Displaying Video: The original video frame with faces outlined, emotion labels, and stress levels is displayed using OpenCV's imshow function. The loop continues until the user presses the 'q' key.
Cleanup: Once the loop is exited, the webcam is released, and all OpenCV windows are destroyed.
