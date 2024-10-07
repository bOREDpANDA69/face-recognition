# Facial Recognition Project

This project uses OpenCV to implement a simple facial recognition system that detects faces in real-time using your webcam. The program uses a pre-trained model based on Haar cascades to identify faces and draw rectangles around them on the video feed.

## Technologies Used

- **Python**: The programming language used for the implementation.
- **OpenCV**: An open-source computer vision library used for real-time image and video processing.
- **Haar Cascades**: Pre-trained classifiers for object detection (in this case, face detection) provided by OpenCV.

## How Facial Recognition Works

The facial recognition process involves the following steps:

1. **Loading the Haar Cascade Classifier**:
   - We use OpenCV's `CascadeClassifier` method to load a pre-trained XML file (`haarcascade_frontalface_default.xml`). This file contains the trained model parameters for detecting frontal faces.

2. **Capturing Video from the Webcam**:
   - The program captures video in real-time using OpenCV's `VideoCapture` method, which accesses your webcam.

3. **Converting the Video Frame to Grayscale**:
   - The video feed is converted to grayscale using `cvtColor` because the Haar cascade works more efficiently with grayscale images.

4. **Detecting Faces**:
   - The `detectMultiScale` method of the classifier scans the grayscale image to find faces. It returns a list of rectangles, each representing the location of a detected face.

5. **Drawing Rectangles Around Faces**:
   - For each detected face, a rectangle is drawn on the original video frame using the coordinates returned by the classifier.

6. **Displaying the Video Feed**:
   - The modified video feed with rectangles drawn around the detected faces is displayed using `imshow`. The program continues to run until the escape key (`ESC`) is pressed.

## Prerequisites

Ensure you have Python installed and the following libraries:

```bash
pip install opencv-python
