# Facial Emotion Detection → Mood-Based Lighting

Real-time facial emotion recognition from a webcam, built as the vision half of a mood-based lighting project: every few seconds the dominant emotion is sent to a local lighting controller API.

**Stack:** Python · TensorFlow / Keras · OpenCV

## How it works

1. OpenCV's Haar cascade detects faces in each webcam frame.
2. The face is cropped, converted to 48×48 grayscale and classified by a CNN (`fed_50epoch.h5`, trained for 50 epochs on FER-2013) into Angry, Disgust, Fear, Happy, Sad, Surprise or Neutral.
3. Predictions above 80% confidence are drawn on the frame.
4. Every 6 seconds the most frequent emotion is POSTed to a local endpoint (`/receive_emotion`) that drives the lights.

## Run it

```bash
pip install tensorflow opencv-python numpy requests
export LIGHTING_API_USER=...   # credentials for the local lighting API
export LIGHTING_API_PASS=...
python cam_cap.py              # press Q to quit
```

Note: this repo contains the inference script and trained model only; the training notebook isn't included.
