# SIGN-LANGUAGE-DETECTION-USING-CNN-LSTM

This repository contains a sign language detection system that recognizes gestures and provides text and voice outputs in English and Tamil. The system utilizes CNNs for feature extraction and LSTMs for sequence learning to ensure high accuracy in gesture recognition.

## Prerequisites

Before you start, make sure you have the following software installed on your system:

- Python 3.x
- pip (Python package installer)
- Virtual environment (optional but recommended)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sign-language-detection.git
   cd sign-language-detection
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

   Create a `requirements.txt` file with the following content:
   ```txt
   opencv-python
   cvzone
   numpy
   pyttsx3
   playsound
   tensorflow
   ```

4. Download the pre-trained model:
   Make sure you have the `keras_model.h5` file in the root directory of your project.

## Running the Scripts

### 1. Data Collection Script

This script captures hand gestures and saves the images in a specified folder.

Usage:
   ```bash
   python Datacollection.py
   ```

Steps:
- Run the script.
- Select the language (e.g., `en` for English).
- Show your hand gesture to the camera.
- Press the `s` key to save the image.

### 2. Gesture Recognition Script

This script recognizes the hand gestures and provides text and voice outputs.

Usage:
   ```bash
   python newtest.py
   ```

Steps:
- Run the script.
- Show your hand gesture to the camera.
- The system will recognize the gesture and provide real-time feedback through text and voice.

## Directory Structure

The directory structure should look like this:
```
sign-language-detection/
│
├── Data/
│   └── Okay/   # Folder for storing captured images
│
├── keras_model.h5
│
├── Datacollection.py
├── newtest.py
├── README.md
├── requirements.txt

```
## Troubleshooting

1. Camera not opening:
   Make sure your webcam is connected and accessible. Check if other applications are using the camera.

2. Missing dependencies:
   Ensure all required packages are installed. Run `pip install -r requirements.txt` again if needed.

3. Model not found:
   Verify that `keras_model.h5` is in the correct directory.

4. Audio issues:
   Make sure your system's audio output is working correctly.

## Acknowledgements

This project uses the following libraries:
- OpenCV for computer vision tasks
- cvzone for hand tracking
- numpy for numerical operations
- pyttsx3 for text-to-speech
- playsound for playing audio files
- tensorflow for deep learning
