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
4. **Run the application**
```bash
python emotion_detection.py
```

5. **For webcam detection**
```bash
python webcam_detection.py
```

---

## 🎮 Usage

### Real-Time Webcam Detection
```python
python webcam_detection.py
# Press 'q' to quit
```

### Single Image Detection
```python
from emotion_detector import EmotionDetector

detector = EmotionDetector()
emotion = detector.predict_emotion('path/to/image.jpg')
print(f"Detected emotion: {emotion}")
```

### Video File Processing
```python
python video_detection.py --input video.mp4 --output result.mp4
```

---

## 🧠 Model Details

### CNN Architecture
```
Input (48x48 grayscale) 
    ↓
Conv2D (32 filters, 3x3) + ReLU
    ↓
MaxPooling (2x2)
    ↓
Conv2D (64 filters, 3x3) + ReLU
    ↓
MaxPooling (2x2)
    ↓
Conv2D (128 filters, 3x3) + ReLU
    ↓
MaxPooling (2x2)
    ↓
Flatten
    ↓
Dense (256) + ReLU + Dropout(0.5)
    ↓
Dense (7) + Softmax
    ↓
Output (7 emotion classes)
```

### Training Details
- **Dataset:** FER-2013 (35,887 images)
- **Image Size:** 48x48 pixels, grayscale
- **Batch Size:** 64
- **Epochs:** 50+
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy

---

## 📊 Performance

| Metric | Score |
|--------|-------|
| Training Accuracy | ~65% |
| Validation Accuracy | ~60% |
| Inference Time | <50ms per frame |
| FPS (Real-time) | 20-30 FPS |

*Note: Accuracy varies based on lighting, face angle, and occlusions*

---

## 🎯 Use Cases

1. **Mental Health Apps** – Mood tracking and emotional wellness
2. **Customer Service** – Sentiment analysis for support calls
3. **Education** – Student engagement monitoring
4. **Marketing Research** – Product response analysis
5. **Gaming** – Emotion-based gameplay adaptation
6. **Human-Computer Interaction** – Adaptive UI based on user emotion
7. **Security Systems** – Detect distress or suspicious behavior

---

## 📸 Example Output
```
Frame: 1024
Detected Face: (x=120, y=80, w=150, h=150)
Emotion: Happy (confidence: 87.3%)
```

---

## 🛠️ Configuration

Edit `config.py` to customize:
```python
# Model settings
MODEL_PATH = 'models/emotion_model.h5'
EMOTION_LABELS = ['Angry', 'Disgust', 'Fear', 'Happy', 'Sad', 'Surprise', 'Neutral']

# Detection settings
FACE_CASCADE_PATH = 'haarcascade_frontalface_default.xml'
CONFIDENCE_THRESHOLD = 0.5

# Display settings
SHOW_CONFIDENCE = True
BOUNDING_BOX_COLOR = (0, 255, 0)
TEXT_COLOR = (255, 255, 255)
```

---

## 🔧 Improving Accuracy

### Tips for Better Results:
- ✅ Good lighting conditions
- ✅ Face directly towards camera
- ✅ Clear, unobstructed face
- ✅ Neutral background
- ❌ Avoid extreme angles
- ❌ Minimize occlusions (glasses, masks)

### Model Improvements:
- Use larger datasets (AffectNet, RAF-DB)
- Data augmentation techniques
- Transfer learning (VGGFace, ResNet)
- Ensemble methods
- Attention mechanisms

---

## 🗺️ Roadmap

- [ ] Improve model accuracy with transfer learning
- [ ] Multi-face detection in single frame
- [ ] Emotion intensity scoring (0-100%)
- [ ] Historical emotion tracking over time
- [ ] Mobile app development (iOS/Android)
- [ ] REST API for cloud deployment
- [ ] Integration with video conferencing platforms
- [ ] Real-time emotion analytics dashboard

---

## 🤝 Contributing

Contributions are welcome! Help improve emotion detection accuracy and features.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/ImprovedModel`)
3. Commit your changes (`git commit -m 'Add attention mechanism'`)
4. Push to the branch (`git push origin feature/ImprovedModel`)
5. Open a Pull Request

---

## 📚 Resources

- [FER-2013 Dataset](https://www.kaggle.com/datasets/msambare/fer2013)
- [OpenCV Face Detection](https://docs.opencv.org/4.x/db/d28/tutorial_cascade_classifier.html)
- [Emotion Recognition Research Papers](https://paperswithcode.com/task/facial-expression-recognition)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Sahil Bhadane**  
- GitHub: [@SahilSBhadane](https://github.com/SahilSBhadane)
- LinkedIn: [linkedin.com/in/sahil-bhadane](https://www.linkedin.com/in/sahil-bhadane)
- Email: sahilbhadane04@gmail.com

---

## 🙏 Acknowledgments

- FER-2013 dataset creators
- OpenCV community
- TensorFlow/Keras documentation
- Research in affective computing

---

<div align="center">

### ⚡ "Understanding emotions through code"

Made with 🎭 for human-computer interaction

</div>
