# Smart-Vision-Attendance-System
## This project was developed as a technical assessment for the Medoc Health selection process.

This project is a Face Recognition based Attendance System that uses a live camera feed to automatically identify registered individuals and record their attendance. It simulates how a real-world biometric entry system works, using computer vision techniques instead of manual sign-in sheets.

The goal of this project is to demonstrate practical understanding of face detection, face recognition, and system-level thinking, not just model training.

## 🧩 Problem Statement

Traditional attendance methods are slow, manual, and prone to errors like proxy attendance. This project aims to automate the process using facial recognition so that attendance can be recorded accurately, quickly, and contactlessly.

## 🧠 System Overview

The system follows this pipeline:

Face Registration → Model Training → Live Recognition → Attendance Logging

Each person’s face images are stored in a dataset. The model learns from these images and later recognizes the person from a webcam feed to mark attendance.

## ✨ Key Features

✔ Real-time face detection using camera

✔ Face recognition using LBPH algorithm

✔ Individual dataset per person

✔ Automatic Punch In on first detection

✔ Manual Punch Out confirmation (press O)

✔ Prevents duplicate attendance entries

✔ Attendance stored in CSV file

✔ Simple, lightweight and runs on CPU

## 🛠 Technologies Used

Python

OpenCV (Computer Vision)

NumPy

Pandas

Haar Cascade Classifier (Face Detection)

LBPH Face Recognizer (Face Recognition)


## 📸 Step 1 — Dataset Collection

Each person has a separate folder inside the dataset directory.
15–20 images per person are captured with different angles and expressions to improve recognition.

## 🤖 Step 2 — Model Training

Faces are extracted from dataset images and used to train an LBPH (Local Binary Pattern Histogram) model. LBPH is chosen because:

Works well on small datasets

Fast and lightweight

Suitable for real-time CPU applications

## 🎥 Step 3 — Real-Time Recognition

The webcam feed is processed frame by frame:

Faces are detected using Haar Cascade

The LBPH model predicts the identity

Confidence threshold ensures accuracy

## 📝 Attendance Logic
Scenario	System Action
Person detected first time	Punch In recorded
Person appears again	System prompts for checkout
User presses O	Punch Out recorded
Duplicate attempts	Ignored
## ▶ How to Run

1. Install dependencies

pip install opencv-python numpy pandas


2. Start Jupyter Notebook

jupyter notebook


3. Open the notebook and:

Run the training cell

Run the attendance system cell

4. Controls

Press O → Punch Out

Press ESC → Exit camera

## 📊 Output File

Student_attendance.csv

Name	Punch In	Punch Out
## ⚠ Limitations

Accuracy may drop in poor lighting

Similar-looking faces may confuse model

No deep learning or anti-spoofing included

## 🔮 Future Improvements

Deep learning face embeddings (FaceNet/ArcFace)

Liveness detection

GUI interface

Cloud/database integration

## 👨‍💻 Author

Rajesh Kinjarapu
AI/ML Internship Assignment Project
