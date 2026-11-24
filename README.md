# 😊 Real-Time Emotion Detection Using Deep Learning

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange?style=for-the-badge&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=for-the-badge&logo=opencv&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white)

![GitHub stars](https://img.shields.io/github/stars/banerjeeanushree7-gif/Real-Time-Emotion-Detection?style=social)
![GitHub forks](https://img.shields.io/github/forks/banerjeeanushree7-gif/Real-Time-Emotion-Detection?style=social)
![GitHub issues](https://img.shields.io/github/issues/banerjeeanushree7-gif/Real-Time-Emotion-Detection)
![GitHub last commit](https://img.shields.io/github/last-commit/banerjeeanushree7-gif/Real-Time-Emotion-Detection)
![GitHub repo size](https://img.shields.io/github/repo-size/banerjeeanushree7-gif/Real-Time-Emotion-Detection)
![GitHub language count](https://img.shields.io/github/languages/count/banerjeeanushree7-gif/Real-Time-Emotion-Detection)
![GitHub top language](https://img.shields.io/github/languages/top/banerjeeanushree7-gif/Real-Time-Emotion-Detection)

---

## 📌 Project Overview

**Real-Time Emotion Detection Using Deep Learning** is a computer vision-based application that detects and recognizes human facial emotions through a live webcam feed.

The system uses a trained Deep Learning model to classify facial expressions into five different emotion categories. OpenCV is used for face detection, image preprocessing and real-time webcam interaction, while TensorFlow/Keras is used to load and execute the trained emotion classification model.

The project demonstrates how Artificial Intelligence and Computer Vision can be applied to facial expression recognition and real-time emotion analysis.

## 🚀 Key Features

### 😊 Emotion Recognition
- Detects five different facial emotions.
- Identifies emotions from live webcam input.
- Uses a trained Deep Learning model.
- Processes facial images in grayscale.
- Resizes facial regions to 48 × 48 pixels.

### 👁️ Face Detection
- Uses Haar Cascade Classifier for face detection.
- Identifies facial regions from webcam frames.
- Draws bounding boxes around detected faces.
- Displays the predicted emotion above the detected face.

### 📷 Real-Time Webcam Processing
- Captures live video through the webcam.
- Processes frames continuously.
- Performs face detection and emotion classification.
- Displays the results in a real-time window.
- Press `Q` to exit the webcam application.

## 🎭 Emotion Categories

The model recognizes the following five emotion categories:

| Emotion | Description |
|---|---|
| 😠 Angry | Detects angry facial expressions |
| 😊 Happy | Detects happy facial expressions |
| 😐 Neutral | Detects neutral facial expressions |
| 😢 Sad | Detects sad facial expressions |
| 😲 Surprised | Detects surprised facial expressions |

## 🧠 Working Methodology

The application follows a sequence of image processing and classification steps:

1. **Webcam Input:** Captures live video frames using OpenCV.
2. **Face Detection:** Detects faces using the Haar Cascade Classifier.
3. **Grayscale Conversion:** Converts detected facial regions into grayscale images.
4. **Image Resizing:** Resizes each facial region to 48 × 48 pixels.
5. **Normalization:** Scales pixel values between 0 and 1.
6. **Emotion Classification:** Passes the processed image to the trained Deep Learning model.
7. **Result Display:** Displays the predicted emotion with a bounding box around the detected face.

## 🛠️ Tech Stack

### Programming Language
- Python

### Deep Learning
- TensorFlow
- Keras

### Computer Vision
- OpenCV
- Haar Cascade Classifier

### Data Processing & Visualization
- NumPy
- Matplotlib
- Pickle

### Development Environment
- Jupyter Notebook
- Anaconda / Python Environment

## 📂 Project Structure

```text
Real-Time-Emotion-Detection/
│
├── Emotion/
│   ├── angry/
│   ├── happy/
│   ├── neutral/
│   ├── sad/
│   └── surprised/
│
├── Data/
│   ├── images.p
│   └── labels.p
│
├── Detection.ipynb
├── Emotion Zip.ipynb
│
├── emotion_detection_model.h5
├── haarcascade_frontalface_default.xml
│
└── README.md
```

## 📊 Dataset Information

The project contains facial expression images organized into five emotion categories.

| Emotion Category | Number of Images |
|---|---:|
| Angry | 3,010 |
| Happy | 4,098 |
| Neutral | 3,027 |
| Sad | 3,027 |
| Surprised | 2,925 |
| **Total** | **16,087** |

### Dataset Preprocessing

The preprocessing notebook performs the following operations:

- Loads images from their respective emotion folders.
- Converts images into grayscale format.
- Resizes images to 48 × 48 pixels.
- Organizes images and their corresponding emotion labels.
- Converts the processed images and labels into NumPy arrays.
- Saves the processed data using Pickle.

## ⚙️ Getting Started

Follow these steps to run the project on your local machine.

### 1. Clone the Repository

```bash
git clone https://github.com/banerjeeanushree7-gif/Real-Time-Emotion-Detection.git
```

### 2. Navigate to the Project Directory

```bash
cd Real-Time-Emotion-Detection
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

### 4. Install Required Libraries

```bash
pip install tensorflow opencv-python numpy matplotlib jupyter
```

### 5. Open Jupyter Notebook

```bash
jupyter notebook
```

### 6. Run the Application

Open `Detection.ipynb` and execute the notebook cells.

Make sure your webcam is connected and accessible.

**Note:** Before running the notebook, update the model and Haar Cascade file paths to match your local project directory. The original notebook contains Windows-specific absolute paths.

For example, use:

```python
from pathlib import Path

BASE_DIR = Path.cwd()

model_path = BASE_DIR / "emotion_detection_model.h5"
cascade_path = BASE_DIR / "haarcascade_frontalface_default.xml"
```

Then load the files using:

```python
from keras.models import load_model
import cv2

model = load_model(str(model_path))

face_cascade = cv2.CascadeClassifier(str(cascade_path))
```

## 📓 Project Notebooks

### 1. Emotion Zip.ipynb
This notebook handles dataset preparation and preprocessing. It reads facial expression images, converts them into grayscale, resizes them and stores the processed images and labels using Pickle.

### 2. Detection.ipynb
This notebook implements real-time facial emotion detection using a webcam. It loads the trained model, detects faces using Haar Cascade and predicts the corresponding emotion.

## 🎯 Learning Outcomes

Through this project, the following concepts were explored:

- Fundamentals of Artificial Intelligence and Deep Learning.
- Facial Expression Recognition.
- Computer Vision and Image Processing.
- Haar Cascade-based Face Detection.
- Image Resizing and Normalization.
- TensorFlow and Keras Model Integration.
- Real-Time Webcam Processing.
- Python-based Machine Learning Applications.

## 🔮 Future Improvements

The project can be further enhanced through:

- Development of a web-based emotion detection application.
- Integration of confidence scores for emotion predictions.
- Improved face detection under different lighting conditions.
- Model optimization for faster real-time processing.
- Support for multiple faces and simultaneous emotion recognition.
- Deployment as an online AI-powered application.

## 🤝 Contributing

Contributions, suggestions and improvements are welcome!

1. Fork this repository.
2. Create a new feature branch.
3. Commit your changes.
4. Push the branch to GitHub.
5. Open a Pull Request.

## 👩‍💻 Author

**Anushree Banerjee**

B.Tech Computer Science & Engineering Student

**Areas of Interest:** Artificial Intelligence | Machine Learning | Deep Learning | Computer Vision

🌐 **LinkedIn:** [Anushree Banerjee](https://www.linkedin.com/in/anushree-banerjee-4086b135a/)

🐙 **GitHub:** [banerjeeanushree7-gif](https://github.com/banerjeeanushree7-gif)

---

<div align="center">

### ⭐ If you find this project interesting, consider giving it a star!

**Built with Python, Deep Learning and Computer Vision.**

</div>
