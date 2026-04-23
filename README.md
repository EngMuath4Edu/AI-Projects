# X-Ray Hairline Fracture Detection Tool (v1.0)

A lightweight image processing pipeline built with Python and OpenCV designed to assist in the visualization of subtle hairline fractures in X-ray imagery. 

## 🔍 Overview
Detecting hairline fractures can be difficult due to low contrast and noise in medical imaging. This tool enhances X-ray images through a multi-stage computer vision pipeline to make these structural anomalies more visible to the human eye.

## 🛠️ Features
*   **Histogram Equalization:** Automatically balances image contrast to bring out details in underexposed areas.
*   **Adaptive Thresholding:** Isolates features based on local pixel intensity rather than a global value.
*   **Canny Edge Detection:** Tuned sensitivity to identify fine, linear patterns characteristic of fractures.
*   **Morphological Refinement:** Uses dilation and erosion to bridge gaps in detected edges and reduce noise.

## 🚀 Getting Started

### Prerequisites
You will need Python installed along with the following libraries:
```bash
pip install opencv-python numpy matplotlib
```

### Installation & Usage
1. Clone this repository to your local machine.
2. Open the script and update the image path:
   ```python
   img = cv2.imread(r'YOUR_PATH\image.jpg', 0)
   ```
3. Run the script:
   ```bash
   python fracture_detection.py
   ```

## 📊 Pipeline Results
The tool outputs a three-panel comparison:
1.  **Original Image:** The raw grayscale input.
2.  **Adaptive Thresholding:** Highlights local structures and potential density changes.
3.  **Processed Edges:** The final output showing refined contours and potential fracture lines.

## ⚠️ Disclaimer
*This tool is for educational and research purposes only. It is not a certified medical diagnostic tool and should not be used as a replacement for professional radiological assessment.*
