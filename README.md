# Virtual Touchscreen Interface for Piano Tiles/OSU Mania

<p align="center">
  <img src="https://github.com/Dericknorlan/handtracking/blob/main/Images/Example.png" alt="">
</p>


A scalable, low-cost virtual touchscreen interface that enables "Piano Tiles"-style gameplay on any flat surface using computer vision. By leveraging standard webcams and a touchless tracking pipeline, this system eliminates the need for expensive or proprietary touch-hardware sensors.

This repository provides a clean implementation utilizing Google **MediaPipe** for hand landmark extraction and **OpenCV** for real-time video processing and visual tracking.

---

## 📌 Key Features
* **Simultaneous Multi-Finger Tracking:** Supports independent detection of the index and middle fingers at the same time (multi-finger input).
* **Touchless Interaction:** Transforms a projection area or flat surface into an interactive virtual touchscreen.
* **Affordable Hardware Compatibility:** Designed to be *hardware-agnostic* so it runs optimally on standard built-in laptop or desktop webcams without additional external sensors.
* **Precise Coordinate Mapping:** Integrates virtual tile segmentation with dynamic screen resolution adjustment.

---

## 📽️ Hardware Schematic
<p align="center">
  <img src="https://github.com/Dericknorlan/handtracking/blob/main/Images/Skema_Hardware.png" alt="">
</p>

---

## 🛠️ System Workflow

This system processes visual data through a closed-loop pipeline that operates in real time:
1. **Camera Capture:** A webcam continuously captures a video stream from the interaction area.
2. **Landmark Detection:** MediaPipe Hands extracts 21 anatomical landmarks of the hand (focusing on the tips of the index and middle fingers).
3. **Tracking & Filtering:** OpenCV performs noise reduction (jitter-smoothing) to maintain coordinate stability between frames.
4. **Action Mapping:** Identifies the position of the fingertips relative to the piano key coordinates (`d`, `f`, `j`, `k`) and simulates keyboard keystrokes using the `keyboard` library.

---

## 🚀 Getting Started

### Prerequisites & Dependencies
Make sure you have Python installed (version 3.8 or later is recommended). Install the required dependencies using the following command and the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### How to Run the Application
1. Connect the webcam to your computer
2. Configure it according to the hardware diagram
3. Run the script:
   
```bash
python main.py
```

---

## Made by
1. [Derick Norlan](https://github.com/Dericknorlan)
2. [Aaron Jevon Benedict Kongdoh](https://github.com/trfyrt)

© Tim Gabut 2026
