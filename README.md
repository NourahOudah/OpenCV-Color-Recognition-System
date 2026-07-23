# OpenCV-Color-Recognition-System
This project uses OpenCV and Python to detect and recognize colors in real-time using a webcam. The system processes the camera frames and identifies red, green, and blue colors, then displays the detected color on the screen
# OpenCV Color Recognition System

## Project Description

This project uses OpenCV and Python to detect and recognize colors in real-time using a webcam. The system captures images from the camera, processes the frames, identifies specific colors (Red, Green, and Blue), and displays the detected color name on the screen.

## Project Objective

The objective of this project is to implement a computer vision application using OpenCV. The project demonstrates how image processing techniques can be used to analyze camera input and recognize colors in real-time.

## Tools and Technologies

- Python
- OpenCV Library
- NumPy Library
- Visual Studio Code
- Anaconda Environment

---

# Installation Steps

## Step 1: Setup the Environment

Anaconda was used as a Python environment to manage the project and install the required libraries.

## Step 2: Install Required Libraries

The following libraries were installed:

```bash
pip install opencv-python
pip install numpy

OpenCV: Used for image processing, accessing the webcam, and displaying results.
NumPy: Used for creating color ranges and processing image data.

⸻

Project Implementation Steps
Step 1: Import Libraries
The project starts by importing the required libraries:

Example:
import cv2
import numpy as np

Step 2: Open the Webcam

The program connects to the computer webcam using OpenCV:
cap = cv2.VideoCapture(0)

This allows the system to capture real-time video frames.

⸻

Step 3: Read Camera Frames

The program continuously reads images from the webcam:
ret, frame = cap.read()

Each frame represents a new image captured from the camera.

⸻

Step 4: Convert Image Format to HSV

The captured image is converted from BGR format to HSV format:

cv2 for computer vision operations.
numpy for numerical operations and defining color ranges.
hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)

HSV format helps the program detect colors more accurately because it separates color information from brightness.

Color Recognition Process

The system recognizes three colors:

1. Red Color Recognition

The program defines a specific range for detecting the red color:

lower_red = np.array([0,120,70])
upper_red = np.array([10,255,255])

The program compares the camera image with this range. If red pixels are detected, the system displays:

Red Color Detected

2. Green Color Recognition

The program defines a range for detecting green color:

lower_green = np.array([40,50,50])
upper_green = np.array([80,255,255])

When green color is detected, the system displays:

Green Color Detected

3. Blue Color Recognition

The program defines a range for detecting blue color:

lower_blue = np.array([90,50,50])
upper_blue = np.array([130,255,255])

When blue color is detected, the system displays:

Blue Color Detected

How the Code Works

The webcam captures real-time images.
OpenCV processes each frame.
The image is converted from BGR to HSV format.
The program checks the image colors using predefined color ranges.
When a matching color is detected, the program displays the color name on the screen.

⸻
How to Run the Project

Open the project folder using Visual Studio Code.
Open the Terminal.
Run the following command:

python main.py

The webcam will open automatically.
Place a colored object in front of the camera.
The system will recognize the color and display its name.
Press the key Q to close the camera window.

Project Files
Color_Recognition_Project

│── main.py
│── README.md

Result

The project successfully detects and recognizes red, green, and blue colors in real-time using OpenCV and a webcam.

⸻
Conclusion

This project demonstrates the use of computer vision techniques with OpenCV to recognize colors from live camera input. It provides a simple example of real-time image processing and color detection.
