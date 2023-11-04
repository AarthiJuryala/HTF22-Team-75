# Sign Language Gesture Recognition System

This repository contains a system that is designed to capture, process, and recognize hand gestures from real-time webcam feeds. It consists of four Python scripts that collectively build a complete sign language gesture recognition pipeline:

1. **`get_img.py`**:
   - Captures images from a webcam in real-time and saves them to the 'DATASET' directory.
   - Continuously captures images until the user presses 'q' or reaches a maximum of 500 images.

2. **`get_data.py`**:
   - Reads static images from the 'DATASET' directory.
   - Extracts landmark data, processes it, and saves it to 'dataset.csv' for use as training data.

3. **`train.py`**:
   - Loads the dataset from 'dataset.csv'.
   - Utilizes a Support Vector Machine (SVM) classifier to train a machine learning model on the hand sign data.
   - Saves the trained SVM model to 'model.pkl' using pickle for real-time ASL gesture recognition.

4. **`hand_reg.py`**:
   - Uses the trained SVM model for real-time hand gesture recognition from a webcam feed.
   - Continuously performs real-time gesture recognition until the user presses 'q'.

## How to Use

1. Clone or download this repository to your local machine.
2. Run the files in the order mentioned above.

## Acknowledgments

- [OpenCV](https://opencv.org/) - For image processing and camera capture.
- [MediaPipe](https://mediapipe.dev/) - For hand landmark detection.
- [scikit-learn](https://scikit-learn.org/) - For machine learning and SVM classifier.
- [Pandas](https://pandas.pydata.org/) - For data manipulation.
- [NumPy](https://numpy.org/) - For numerical computations.
