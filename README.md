# Real-Time Video Processing Framework using OpenCV

A multi-threaded real-time video processing framework developed in Python using OpenCV for 720p live video enhancement and analysis. The framework provides interactive image enhancement, edge detection, performance monitoring, and side-by-side visualization without requiring dedicated hardware acceleration.

## Features

- Real-time 720p video processing
- Brightness and contrast adjustment
- Grayscale conversion
- Sharpening filter
- Box blur filter
- Gaussian blur filter
- Emboss filter
- Negative transformation
- Morphological dilation
- Sobel edge detection
- Canny edge detection
- Side-by-side display of original and processed frames
- Frame capture functionality
- Real-time FPS monitoring
- Multi-threaded architecture for improved responsiveness
- Modular design for future FPGA acceleration

## System Architecture


Camera Input
      │
      ▼
Frame Acquisition (OpenCV)
      │
      ▼
Pre-processing
(Brightness, Contrast, Grayscale)
      │
      ▼
Image Enhancement
 ├── Sharpen
 ├── Box Blur
 ├── Gaussian Blur
 ├── Emboss
 ├── Negative
 ├── Dilation
 ├── Sobel Edge Detection
 └── Canny Edge Detection
      │
      ▼
Visualization
(Side-by-Side Display)
      │
      ├── Frame Capture
      └── FPS Monitoring Thread


## Technologies Used

- Python 3.x
- OpenCV
- NumPy
- Tkinter
- Multi-threading

## Installation

Clone the repository:

```bash
git clone https://github.com/username/repository-name.git
cd repository-name
```

Install dependencies:

```bash
pip install opencv-python numpy pillow
```

## Usage

Run the application:

```bash
python main.py
```

The GUI allows users to:

- Select different processing modes
- Adjust brightness and contrast
- Enable grayscale conversion
- Capture processed frames
- Monitor FPS in real time
- Compare original and processed outputs

## Performance

| Processing Mode | FPS | Speedup |
|----------------|-----|----------|
| Sharpen | ~17 FPS | 1.57× |
| Sobel Edge Detection | ~18.98 FPS | 1.40× |
| Canny Edge Detection | ~20.95 FPS | 1.81× |

### Image Quality Metrics

- PSNR: 30.22 dB
- SSIM: 0.898
- SNR: 26.20 dB

## Applications

- Intelligent surveillance
- Computer vision systems
- Robotics and autonomous navigation
- Industrial inspection
- Edge AI devices
- Machine vision
- Image enhancement and analysis
- Academic research

## Future Work

- FPGA hardware acceleration
- PYNQ-Z2 implementation
- Hardware-software co-design
- GPU acceleration
- Deep learning-based enhancement
- Object detection and tracking
- Semantic segmentation

## Authors

- **Soujit Chel**  
  Department of Electronics and Telecommunication Engineering  
  KIIT University, Bhubaneswar, India

- **Jhilam Jana**  
  Department of CSE (AI & ML)  
  Institute of Engineering & Management, Kolkata, India

- **Sayan Tripathi**  
  Department of CSE (AI & ML)  
  Institute of Engineering & Management, Kolkata, India

## Citation

If you use this work in your research, please cite:

```bibtex
@article{chel2026realtimevideo,
  title={Design and Implementation of a Real-Time Video Processing Framework Using OpenCV-Based Spatial Filtering and Multi-Thread Python Architecture},
  author={Chel, Soujit and Jana, Jhilam and Tripathi, Sayan},
  year={2026}
}
```

## License

This project is released under the MIT License.

---

**Keywords:** OpenCV, Real-Time Video Processing, Image Enhancement, Edge Detection, Multi-Threading, Computer Vision, FPS Monitoring, Python, Image Filtering, Machine Vision.
