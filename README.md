# 🚗 Drive Care – A Driver Drowsiness Detection System

### 📌 Project Overview
Drive Care is a real-time **driver drowsiness detection system** that uses **computer vision** techniques to detect signs of drowsiness in drivers and alert them, reducing the risk of accidents. The system monitors the driver's **eye aspect ratio (EAR)** and **yawning patterns** to determine signs of fatigue.

## 📋 Problem Statement
According to the **National Sleep Foundation**, around **32% of drivers experience drowsy driving at least once a month**, contributing to **25% of all traffic accidents annually**. Existing laws and regulations **do not provide real-time detection** of fatigue, making an **automated drowsiness detection system** crucial.

## 🎯 Objectives
- Detect **driver drowsiness in real time** using a webcam.
- Alert the driver when signs of drowsiness (eye closure/yawning) are detected.
- Implement a **non-intrusive and efficient solution** using machine learning and computer vision.

---

## ⚙️ Technologies Used
- **Programming Language:** Python
- **Libraries:**
  - [OpenCV](https://opencv.org/) – Image processing and computer vision
  - [Dlib](http://dlib.net/) – Facial landmark detection
  - [Imutils](https://pypi.org/project/imutils/) – Image processing utilities
  - [Numpy](https://numpy.org/) – Numerical computations

---

## 🏗️ Algorithm Overview

1. **Initialize Webcam** – Capture real-time video stream.
2. **Detect Face and Eyes** – Use `Dlib`’s pre-trained 68-facial landmark detector.
3. **Calculate Eye Aspect Ratio (EAR)**:
   - If **EAR < 0.25** for a certain number of frames → **Drowsiness detected!**
   - If **Yawning detected for >15 sec** → **Drowsiness detected!**
4. **Trigger an Alarm** – Audio alert is played when drowsiness is detected.

### 📌 Eye Aspect Ratio (EAR) Formula:
\[
EAR = \frac{‖P2 - P6‖ + ‖P3 - P5‖}{2 \times ‖P1 - P4‖}
\]
- If **EAR > 0.25** → Eyes **Open**
- If **EAR ≤ 0.25** → Eyes **Closed** (possible drowsiness)

---

## 🛠️ Installation Guide

### 1️⃣ Prerequisites
Make sure you have **Python 3.7+** installed on your system. You can download it from [here](https://www.python.org/downloads/).

### 2️⃣ Clone the Repository
```sh
git clone https://github.com/yourgithubrepo/driver-drowsiness-detection.git
cd driver-drowsiness-detection
