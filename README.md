Sign Language Detection ✋🤖
This project implements a real-time sign language detection system using computer vision and deep learning to recognize hand gestures for letters (A-E) of the alphabet. It leverages MediaPipe for hand landmark detection and a Keras LSTM model for gesture classification. 📹💻
Features 🌟

Real-time hand gesture detection using a webcam. 📸
Recognition of sign language letters A, B, C, D, and E. 🔤
Visual feedback with probability visualization for detected gestures. 📊
Data collection and preprocessing scripts for training the model. 🗂️

Prerequisites ✅

Python 3.8+ 🐍
Webcam for real-time detection 📷
Required Python packages (see Dependencies 📦)

Installation 🛠️

Clone the repository 📥:
git clone https://github.com/your-username/sign-language-detection.git
cd sign-language-detection


Set up a virtual environment (optional but recommended) 🌀:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install dependencies 📦:
pip install -r requirements.txt

If requirements.txt is not provided, install the packages listed in Dependencies.

Download or train the model 🧠:

The application expects model.json and model.keras files in the root directory. 📂
To train your own model, use the data collection scripts and a separate training script (not provided in the current codebase). 🏋️‍♂️



Usage 🚀

Collect training data (if needed) 📷:

Run dataCollection.py to capture images for signs A-Z:
python dataCollection.py


Press the corresponding letter key (e.g., 'a' for A) to save images to the Image/ directory. 🖼️
Images are saved in subdirectories named A, B, etc. 📁


Process collected images to generate keypoints with data.py:
python data.py


This script reads images from Image/ and saves keypoints to MP_DATA/. 💾




Run the sign language detection 🎥:

Ensure model.json and model.keras are in the root directory. ✅
Execute app.py:python app.py


The webcam feed will open, showing a region of interest (ROI) for hand detection. 🖥️
Detected signs (A-E) and their confidence scores are displayed in the top-left corner. 📈
Press q to exit. 🚪



File Descriptions 📜

app.py 🖥️: Main application script for real-time sign language detection using a pre-trained Keras LSTM model and MediaPipe hand tracking.
function.py 🛠️: Utility functions for MediaPipe detection, landmark drawing, and keypoint extraction.
data.py 📊: Script for processing collected images to extract keypoints and save them as NumPy arrays in MP_DATA/.
dataCollection.py 📸: Script for capturing webcam images for signs A-Z, saving them to the Image/ directory.

Dependencies 📦
Install the following Python packages:
pip install opencv-python numpy mediapipe keras tensorflow

Contributing 🤝
Feel free to open issues or submit pull requests to improve the project! 🌈
License 📝
