# 🖼️ Interactive Image Processing Tool (PyQt5 & OpenCV)
## (Real-time Computer Vision Desktop Application)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyQt5](https://img.shields.io/badge/GUI-PyQt5-green)
![OpenCV](https://img.shields.io/badge/Library-OpenCV-orange)

## 📌 Overview
This is a professional **PyQt5-based desktop application** that bridges the gap between raw OpenCV algorithms and a user-friendly interface. It allows users to perform complex Image Processing tasks interactively with **real-time parameter tuning** using sliders. 

This tool is designed for experimenting with computer vision filters, transformations, and segmentation techniques without writing a single line of code during execution.

---

## 🎯 Key Features

### 1. Edge Detection Suite
* **Advanced Algorithms:** Implementation of **Canny, Sobel, Prewitt, Roberts**, and **Laplacian of Gaussian (LoG)**.
* **Real-time Tuning:** Dynamic sliders to adjust gradient sensitivity and thresholds.

### 2. Smoothing & Denoising
* Comprehensive spatial filters including **Gaussian Blur, Median Filtering, Mean (Averaging)**, and **Bilateral Filtering** (Edge-preserving smoothing).

### 3. Segmentation & Thresholding
* **Adaptive Logic:** Includes **Otsu's Binarization**, **Adaptive Thresholding**, and **Histogram-based segmentation** (essential for OCR and object detection preprocessing).

### 4. Geometric & Morphological Operations
* **Transformations:** Interactive **Rotation** and **Translation**.
* **Morphology:** **Erosion, Dilation, Opening**, and **Closing** for noise removal and shape analysis.

---

## 🏗 Engineering Challenges & Solutions

* **Sequential State Management:** * *Challenge:* Applying multiple filters sequentially without losing the previous effect.
    * *Solution:* Architected a **State Buffer System** (`last_processed_image`) that allows users to stack effects (e.g., Blur → Canny) seamlessly.
    
* **UI-to-Algorithm Synchronization:** * *Challenge:* Mapping continuous slider values to discrete/odd OpenCV kernel sizes.
    * *Solution:* Developed a middleware logic to validate and map GUI inputs to valid mathematical parameters in real-time.

---

## 🚀🛠 Technologies Used
* **Python:** Core programming logic.
* **PyQt5:** Professional GUI development and Event-driven architecture.
* **OpenCV:** High-performance computer vision library.
* **NumPy:** Numerical matrix computations for image arrays.

---

## 📖 How to Use
1. **Load Image:** Click the button to upload any JPG/PNG.
2. **Experiment:** Adjust sliders to apply filters and transformations instantly.
3. **Reset:** Revert to the original image at any time.
4. **Save:** Export your final processed image.

---

## ⚙️ Installation
```bash
# Clone the repository
git clone [https://github.com/markwael/PyQt5-Image-Tool.git](https://github.com/markwael/PyQt5-Image-Tool.git)

# Install dependencies
pip install PyQt5 opencv-python numpy

# Run the application
python main.py
