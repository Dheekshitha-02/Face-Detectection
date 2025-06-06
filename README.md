# Face-Detectection
This project is a Python Flask-based web application that performs real-time face and eye detection using OpenCV and Haar Cascade classifiers. It supports both webcam-based detection and image upload-based detection through a browser interface.

## 🌟 Features
-🧠 Face detection from uploaded images
-👁️ Eye detection via webcam feed
-🎛️ Simple Flask web interface with routes for each function
-🧩 Uses Haar cascade classifiers from OpenCV
-💾 Handles image upload securely and efficiently

## 🗂️ File Structure
bash
```
face-eye-detection-app/
├── index.py                        # Flask application entry point
├── face_eye_detect.py             # Webcam-based face & eye detection
├── detect_face_image.py           # Image upload face detection logic
├── haarcascade_frontalface_default.xml  # Face detection model
├── /templates/
│   ├── index.html
│   ├── form.html
│   └── team_members.html
├── /img/                          # Folder where uploaded images are saved
├── /static/                       # CSS or JS files (if used)
```
## 🚀 How to Run
### 1. Install Requirements
Make sure you have OpenCV and Flask installed:

bash
```
pip install opencv-python flask pillow
```
### 2. Run the Flask App
bash
```
python index.py
```
### 3. Access in Browser
Open http://127.0.0.1:5000

## 🖼️ Functional Overview
📸 Image-Based Face Detection
- Route: /detect_face
- Upload an image via form.html
- Detected faces will be outlined in blue rectangles

🎥 Webcam-Based Face and Eye Detection
- Route: /face_eye
- Accesses webcam via OpenCV
- Detects and draws:
  - Blue rectangle for face
  -  Green rectangles for eyes
- Press q to exit webcam detection

## 🧠 Detection Models Used
- haarcascade_frontalface_default.xml (face detection)
- haarcascade_eye.xml (included via OpenCV internally)

## 📌 Notes
- Make sure your system webcam works for real-time detection
- Uploaded images are saved in the img/ directory
- Windows users may need to allow access to the camera and server ports



