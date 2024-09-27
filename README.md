# Number_of_punch_Pose_Detection_mediapipe
This program uses OpenCV and MediaPipe to capture live video from the webcam and track body pose landmarks. It calculates the angles at the left and right elbows using three points The program counts the number of "punches" 
Here's a simple `README.md` file for the provided program:

# Real-Time Pose Estimation and Punch Counter

This project tracks human body pose in real-time using a webcam, calculating the angles at the elbows and counting "punches" based on arm movement. The solution uses OpenCV for capturing video and MediaPipe for pose estimation.

## Features

- Detects body landmarks and calculates the angle between the shoulder, elbow, and wrist for both arms.
- Counts repetitions ("punches") based on elbow movement.
- Displays the real-time angle and repetition count on the video feed.

## Requirements

- Python 3.x
- Required libraries:
  - `opencv-python`
  - `mediapipe`
  - `numpy`

## Installation

1. Clone or download this repository.
2. Install the required dependencies:

   ```bash
   pip install opencv-python mediapipe numpy
   ```

## Usage

1. Run the Python script:

   ```bash
   python pose_estimation_punch_counter.py
   ```

2. The program will start capturing video from your webcam. It will track your body landmarks and display the angle at the elbow for both arms in real-time.
3. The punch counter increments when the arm is fully extended after being in the bent position.

4. Press `q` to exit the program.

## Key Details

- **Angle Calculation**: The angle between the shoulder, elbow, and wrist is calculated using basic trigonometry.
- **Punch Counter**: A "punch" is counted when the elbow angle moves from a flexed position (less than 60°) to a fully extended position (greater than 160°).
- **User Interface**: The video feed displays the current elbow angles and repetition counts on the screen.

## Troubleshooting

- Ensure your webcam is working properly.
- The `mediapipe` pose detection requires decent lighting and clear visibility of your arms for accurate landmark detection.
