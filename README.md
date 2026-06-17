# Real-Time Video Processing Framework using OpenCV-Based Spatial Filtering and Multi-Thread Python Architecture

![Python](https://img.shields.io/badge/Python-3.x-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![NumPy](https://img.shields.io/badge/NumPy-Scientific_Computing-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Overview

This repository presents a **multi-threaded real-time video processing framework** developed using **Python and OpenCV** for interactive image enhancement and feature extraction. The framework processes 720p live video streams and provides multiple filtering and edge detection operations with real-time parameter control and performance monitoring.

The system combines image enhancement, frame capture, FPS monitoring, and side-by-side visualization within a single modular software architecture. Independent threads are used for video processing and performance evaluation to achieve responsive and low-latency operation.

The framework serves as a software prototype and can be extended to FPGA or hardware-software co-design platforms in future implementations.

---

# Features

### Image Enhancement

* Brightness control
* Contrast control
* Grayscale conversion
* Negative image transformation
* Sharpening filter
* Box blur
* Gaussian blur
* Emboss filter
* Filter2D + Morphological Dilation

### Feature Extraction

* Sobel edge detection
* Canny edge detection

### User Interface

* Interactive GUI
* Real-time mode selection
* Side-by-side display
* Frame capture
* Runtime parameter adjustment

### Performance Analysis

* FPS monitoring
* Speedup estimation
* PSNR computation
* MSE calculation
* SNR measurement
* SSIM evaluation
* Edge Preservation Index (EPI)
* Edge density analysis

---

# Applications

* Intelligent surveillance
* Computer vision systems
* Robotics
* Industrial inspection
* Image enhancement
* Smart cameras
* Edge computing
* Machine vision
* FPGA hardware acceleration research

---

# System Architecture

```
Camera Input
      │
      ▼
Frame Acquisition Module
(OpenCV Video Capture)
      │
      ▼
Pre-processing Module
├── Brightness Adjustment
├── Contrast Adjustment
└── Grayscale Conversion
      │
      ▼
Image Enhancement Module
├── Sharpen
├── Box Blur
├── Gaussian Blur
├── Emboss
├── Negative Transformation
├── Filter2D + Dilation
├── Sobel Edge Detection
└── Canny Edge Detection
      │
      ▼
Visualization Module
(Side-by-Side Display)
      │
      ├── Frame Capture
      └── FPS Monitoring Thread
      │
      ▼
Processed Output
```

---

# Technologies Used

| Component            | Technology      |
| -------------------- | --------------- |
| Language             | Python          |
| Image Processing     | OpenCV          |
| Numerical Operations | NumPy           |
| GUI                  | Tkinter         |
| Parallelism          | Multi-threading |
| Video Source         | Webcam          |
| Resolution           | 1280×720        |

---

# Installation

Clone the repository

```bash
git clone https://github.com/username/repository-name.git
cd repository-name
```

Install dependencies

```bash
pip install opencv-python numpy pillow
```

Run

```bash
python main.py
```

---

# Processing Modes

## Sharpen Filter

Kernel:

```
0  -1   0
-1  5  -1
0  -1   0
```

Purpose:

* Enhance fine details
* Improve edge sharpness

Output:

```text
images/sharpen_output.png
```

---

## Box Blur

Purpose:

* Remove noise
* Smooth image

Output:

```text
images/box_blur_output.png
```

---

## Gaussian Blur

Purpose:

* Preserve edges
* Reduce Gaussian noise

Output:

```text
images/gaussian_output.png
```

---

## Emboss Filter

Purpose:

* Create 3D texture appearance

Output:

```text
images/emboss_output.png
```

---

## Negative Transformation

Purpose:

* Increase intensity contrast

Output:

```text
images/negative_output.png
```

---

## Filter2D + Dilation

Purpose:

* Improve structural continuity

Output:

```text
images/dilation_output.png
```

---

## Sobel Edge Detection

Gradient magnitude:

```
G = √(Gx² + Gy²)
```

Purpose:

* Fast gradient extraction

Output:

```text
images/sobel_output.png
```

---

## Canny Edge Detection

Stages:

1. Gaussian smoothing
2. Gradient computation
3. Non-maximum suppression
4. Double thresholding
5. Hysteresis

Output:

```text
images/canny_output.png
```

---

# Performance Metrics

### FPS

```
FPS = Number of Frames / Elapsed Time
```

### Quality Metrics

* PSNR
* SSIM
* SNR
* MSE
* EPI
* Edge Density

---

# Experimental Setup

| Parameter       | Value          |
| --------------- | -------------- |
| Language        | Python         |
| Library         | OpenCV         |
| Resolution      | 1280×720       |
| Video Source    | Webcam         |
| Processing Type | Software Only  |
| Architecture    | Multi-threaded |

---

# Results

## Sharpen Filter

| Metric  | Value    |
| ------- | -------- |
| PSNR    | 30.22 dB |
| MSE     | 61.75    |
| SNR     | 26.20 dB |
| SSIM    | 0.898    |
| Speedup | 1.57×    |

Image:

```
images/result_sharpen.png
```

---

## Sobel Edge Detection

| Metric       | Value |
| ------------ | ----- |
| FPS          | 18.98 |
| Speedup      | 1.40× |
| EPI          | 0.042 |
| Edge Density | 0.933 |

Image:

```
images/result_sobel.png
```

---

## Canny Edge Detection

| Metric       | Value |
| ------------ | ----- |
| FPS          | 20.95 |
| Speedup      | 1.81× |
| EPI          | 0.017 |
| Edge Density | 0.032 |

Image:

```
images/result_canny.png
```

---

# Performance Comparison

| Operation           | Complexity | Characteristics       |
| ------------------- | ---------- | --------------------- |
| Sharpen             | Moderate   | Detail enhancement    |
| Box Blur            | Low        | Noise suppression     |
| Gaussian Blur       | Moderate   | Smooth output         |
| Emboss              | Moderate   | Texture enhancement   |
| Filter2D + Dilation | Moderate   | Structural continuity |
| Sobel               | Low        | Fast edge extraction  |
| Canny               | High       | Accurate boundaries   |

---

# GUI Output

The application provides:

* Live video display
* Side-by-side comparison
* FPS display
* Quality metrics
* Runtime filter selection
* Brightness and contrast sliders
* Threshold adjustment
* Frame capture functionality

Place screenshots inside:

```
images/gui.png
images/brightness.png
images/negative.png
images/filter2d_dilate.png
images/sobel_gui.png
images/canny_gui.png
```

---

# Repository Structure

```
Real-Time-Video-Processing/
│
├── main.py
├── requirements.txt
├── README.md
├── images/
│     ├── gui.png
│     ├── sharpen_output.png
│     ├── gaussian_output.png
│     ├── emboss_output.png
│     ├── negative_output.png
│     ├── sobel_output.png
│     ├── canny_output.png
│     └── result_sharpen.png
│
├── captured_frames/
└── docs/
```

---

# Future Scope

* GPU acceleration
* FPGA implementation
* PYNQ-Z2 deployment
* Hardware-software co-design
* Object detection
* Object tracking
* Semantic segmentation
* Deep learning enhancement
* Edge AI systems

---

# Authors

### Soujit Chel

Department of Electronics and Telecommunication Engineering
KIIT University, Bhubaneswar, India

### Jhilam Jana

Department of CSE (AI & ML)
Institute of Engineering and Management, Kolkata, India

### Sayan Tripathi

Department of CSE (AI & ML)
Institute of Engineering and Management, Kolkata, India

---

# Citation

```bibtex
@article{chel2026video,
title={Design and Implementation of a Real-Time Video Processing Framework Using OpenCV-Based Spatial Filtering and Multi-Thread Python Architecture},
author={Soujit Chel and Jhilam Jana and Sayan Tripathi},
year={2026}
}
```

---

## License

MIT License
