# 📷 Cheating Detection System Using Computer Vision

## 📌 Overview

The **Cheating Detection System** is a real-time AI-powered online proctoring application that monitors examinees through a webcam and identifies suspicious activities during online examinations. The system combines **computer vision**, **deep learning**, **object detection**, and **facial landmark analysis** to analyze user behavior and estimate a cheating score in real time.

The application detects multiple persons, prohibited objects such as mobile phones and books, abnormal face positioning, and excessive lip movement that may indicate talking during an examination.

---

## 🚀 Features

### 👥 Multiple Person Detection
- Detects the presence of more than one person in the camera frame.
- Flags potential cheating when additional people are detected.

### 📱 Prohibited Object Detection
- Detects mobile phones.
- Detects books and study materials.
- Uses the pre-trained **SSD MobileNet V2** model for real-time object detection.

### 😀 Face Monitoring
- Detects whether the examinee's face is visible.
- Identifies abnormal face positioning.
- Warns when the face leaves the camera frame.

### 👄 Lip Movement Detection
- Uses **Dlib facial landmarks** to monitor mouth movement.
- Performs an initial calibration to determine the user's closed-mouth position.
- Detects excessive mouth opening that may indicate talking.

### 📊 Cheating Score Calculation
- Combines multiple detection signals into a unified cheating score.
- Continuously updates the cheating percentage during monitoring.

### 📈 Real-Time Visualization
- Displays live detection results on the video feed.
- Plots the cheating percentage over time.

---

## 💡 Motivation

With the growing adoption of online examinations, maintaining academic integrity has become increasingly important. This project explores how computer vision and deep learning techniques can automatically identify suspicious behaviors during remote assessments, reducing the need for continuous manual monitoring.

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Computer Vision | OpenCV |
| Facial Landmark Detection | Dlib |
| Object Detection | TensorFlow Hub |
| Detection Model | SSD MobileNet V2 |
| Numerical Computing | NumPy |
| Data Visualization | Matplotlib |
| Scientific Computing | SciPy |

---

## 📂 Project Structure

```text
cheating_detection/
│
├── cheating_detection.py
├── requirements.txt
├── README.md
├── model/
│   └── saved_model/
└── utils/
```

> **Note:** The directory structure may differ slightly depending on your local setup.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/ritusagar225/cheating_detection.git
```

### 2. Navigate to the project directory

```bash
cd cheating_detection
```

### 3. (Optional) Create a virtual environment

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install dependencies

Using the requirements file:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install opencv-python dlib tensorflow tensorflow-hub matplotlib numpy scipy
```

---

## ▶️ Running the Project

Run the application using:

```bash
python cheating_detection.py
```

> **Note:** A webcam is required for real-time monitoring. Without a connected camera, the application cannot capture or analyze video.

---

## 🔄 System Workflow

```text
                 Webcam Input
                      │
                      ▼
               Frame Capture
                      │
      ┌───────────────┼────────────────┐
      │               │                │
      ▼               ▼                ▼
Object Detection   Face Detection   Facial Landmarks
      │               │                │
      │               │                ▼
      │               │         Lip Movement
      │               │
      └───────────────┼────────────────┘
                      ▼
         Cheating Score Calculation
                      │
                      ▼
     Live Alerts & Real-Time Visualization
```

---

## 📊 Detection Indicators

| Detection | Description |
|-----------|-------------|
| Multiple Person Detection | Detects additional people in the camera frame |
| Phone Detection | Detects mobile phones |
| Book Detection | Detects books or study materials |
| Face Missing | Detects when the user's face is not visible |
| Face Position | Detects abnormal head or face positioning |
| Lip Movement | Detects excessive mouth opening that may indicate talking |

The system combines these indicators to estimate the overall likelihood of cheating.

---

## ⚠️ Current Limitations

- Requires a webcam for real-time monitoring.
- Detection performance depends on lighting conditions and camera quality.
- Object detection is limited to the classes supported by the pre-trained SSD MobileNet V2 model.
- Lip movement detection accuracy may decrease when the face is partially occluded or captured at low resolution.

---

## 🚀 Future Improvements

- Eye gaze tracking
- Head pose estimation
- Audio-based speech detection
- Browser tab-switch monitoring
- Candidate face recognition
- Examination report generation
- Web deployment using Flask or FastAPI
- Improved deep learning models for behavior analysis

---

## 🎯 Applications

- Online examinations
- Remote learning platforms
- University assessments
- Coding interviews
- Recruitment tests
- Professional certification exams

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.

```bash
git checkout -b feature-name
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push the branch.

```bash
git push origin feature-name
```

5. Open a Pull Request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👩‍💻 Author

**Ritu Kumari**

Graduate, National Institute of Technology (NIT) Silchar

**Skills:** Python • Computer Vision • OpenCV • TensorFlow • Dlib • Deep Learning • Machine Learning

---

⭐ If you found this project helpful, consider giving it a star!
