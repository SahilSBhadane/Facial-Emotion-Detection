# 🎭 Facial Emotion Detection

### Real-Time Emotion Recognition Using Deep Learning

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)]()
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)]()

---

## 🎯 Overview

A real-time facial emotion detection system that identifies and classifies human emotions from video streams using deep learning and computer vision techniques.

### Detected Emotions

😊 **Happy** | 😢 **Sad** | 😠 **Angry** | 😨 **Fear** | 😐 **Neutral** | 😲 **Surprise** | 🤢 **Disgust**

---

## 🚀 Tech Stack

- **Deep Learning:** TensorFlow/Keras, CNN Architecture
- **Computer Vision:** OpenCV
- **Language:** Python
- **Dataset:** FER-2013 (Facial Expression Recognition)

---

## ⚡ Features

✅ **Real-Time Detection** – Process video streams in real-time  
✅ **7 Emotion Classes** – Comprehensive emotion recognition  
✅ **Face Detection** – Automatic face localization in frame  
✅ **High Accuracy** – Trained on FER-2013 dataset  
✅ **Webcam Support** – Works with any standard webcam  
✅ **Lightweight Model** – Fast inference for real-time applications  

---

## 🏗️ Architecture
```
┌──────────────┐
│  Video Input │ → Webcam or video file
└──────┬───────┘
       │
       ↓
┌──────────────────┐
│  Face Detection  │ → Haar Cascade / MTCNN
└──────┬───────────┘
       │
       ↓
┌──────────────────────┐
│  Preprocessing       │ → Grayscale, resize, normalize
└──────┬───────────────┘
       │
       ↓
┌──────────────────────┐
│  CNN Model           │ → Emotion classification
│  - Conv Layers       │
│  - Pooling           │
│  - Dense Layers      │
└──────┬───────────────┘
       │
       ↓
┌──────────────────────┐
│  Emotion Output      │ → Display predicted emotion
└──────────────────────┘
```

---

## 💻 Installation & Setup

### Prerequisites
- Python 3.7+
- Webcam (for real-time detection)
- pip package manager

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/SahilSBhadane/Facial-Emotion-Detection.git
cd Facial-Emotion-Detection
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Download pre-trained model** (if not included)
```bash
# Model will be in /models
