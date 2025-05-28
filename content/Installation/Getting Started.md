---
title: Getting Started
draft: false
tags: 
description: Describes the first steps to installation.
date: 2025-05-27
aliases:
  - Install
  - Installation
---
## 📖 Overview

IcarusEye is a real-time object detection & tracking system built with:  
- **Model:** YOLOv8s (trained on VisDrone2019-DET)  
- **Tracker:** ByteTrack  
- **UI:** PyQt6 for live controls & display
- **Backend:** OpenCV for video processing
- **Optional:** FFmpeg for extended video support  

The purpose of IcarusEye is to provide a lightweight, easy-to-use solution for real-time object detection and tracking across various applications, with a focus on performance and flexibility.

> [!TIP]  
> Installing **ffmpeg** on your system unlocks full video support (RTSP, USB cams, file formats).

---

## 🛠️ Installation Methods

### Windows
#### 1. Using PyInstaller (Pre-Compiled Executable) 
Download the latest release from the [Releases page](https://github.com/JonathanLTurner03/IcarusEye/releases).
> [!WARNING]
> The compiled version is not available anymore and will be reintroduced in the future.

#### 2. Build From Source
```bash
# Clone the Repository
git clone https://github.com/JonathanLTurner03/IcarusEye.git
cd IcarusEye

# Create a virtual environment
python -m venv .venv
# Activate the virtual environment
.venv/bin/activate.exe

# Install required packages
pip install -r requirements.txt
# Run the application
python main.py
```
> [!TIP]
> If you are utilizing a NVIDIA GPU, ensure you have the latest [CUDA Toolkit](https://developer.nvidia.com/cuda-downloads) installed for optimal performance, along with installing the [PyTorch CUDA version](https://pytorch.org/get-started/locally/) that matches your CUDA version.

> [!NOTE]
> If you encounter issues with the virtual environment, ensure you have Python 3.8+ installed and that your PATH is set correctly.

### Linux

#### Build From Source
```bash
# Clone the project
git clone https://github.com/JonathanLTurner03/IcarusEye.git
cd IcarusEye

# Create and activate the virtual environment
python -m venv .venv
source .venv/bin/activate

# Install required packages
pip install -r requirements.txt

# Run the application
python main.py
```
> [!TIP]
> If you are using a NVIDIA GPU, ensure you have the latest [CUDA Toolkit](https://developer.nvidia.com/cuda-downloads) installed for optimal performance, along with installing the [PyTorch CUDA version](https://pytorch.org/get-started/locally/) that matches your CUDA version.

---

## ⚡ Quick Start

When first launching the program, you will see the main interface with options to select a video source (camera or file) and configure detection settings.

### 1. Select Video Source
- **Camera:** Choose from available cameras (USB, RTSP, etc.)
- **File:** Select a video file from your system.

### 2. Configure Detection Settings
- **Confidence Threshold:** Adjust the confidence threshold for detections.
- **Omitted Classes:** Select classes to ignore (e.g., pedestrians, vehicles).
- **Tracker Settings:** Enable/disable tracking and adjust parameters.
* _etc._

### 3. Start Detection
Click the **Play** button to begin playing the feed, with real-time detection and tracking. The interface will display detected objects with bounding boxes and labels.


## 🎯 Common Use Cases

This project was developed as a means of running object detection and tracking on edge devices, optimizing usability and performance over precision. It is strongly focused with human overview, not automatic and autonomous detection. However, in testing, there are many industries that can benefit from this technology, including:

- **Search & Rescue:** Detect and track individuals in emergency situations.
- **Security & Surveillance:** Monitor live feeds for intrusions or suspicious activity.
- **Retail Analytics:** Track customer movement and behavior in stores.
- **Traffic Monitoring:** Analyze vehicle flow and detect traffic violations.
- **Wildlife Conservation:** Monitor animal populations and behaviors in natural habitats.
- **Sports Analytics:** Track player movements and performance metrics during games.

---

## 🔗 Next Steps

- Dive into [[Configuration]] for advanced tuning  
- Explore the [[API Reference]] to embed IcarusEye in your own app  
- Check the [[Changelog]] to see what’s new each release  
