# currency-detection-
AN AI DEEP LEARNING MODEL TO DETECT FAKE NOTES
# 💵 Currency Detection and Recognition Model

## 🌟 Overview

This project implements a computer vision model (either an **Image Classifier** or an **Object Detector**) designed to accurately identify and recognize different denominations of a target currency from images.

The primary goals of this model are:
1. **Denomination Recognition:** Identifying the value (e.g., 10, 20, 100) of a banknote.
2. **Real-time Detection:** Enabling quick and accurate recognition, potentially for use in mobile applications or automated counting systems.
3. **Robustness:** Handling variations in angle, lighting, and minor wear/tear.

## 📁 Dataset

The model is trained on a custom dataset of currency images.

| Feature | Detail |
| :--- | :--- |
| **Source** | Customly collected images (or specified public dataset like Banknote Authentication Data Set, if used) |
| **Classes** | Each valid denomination (e.g., $10, $20, $50, $100) plus a background/invalid class (if using Object Detection). |
| **Total Images** | [**INSERT YOUR TOTAL IMAGE COUNT HERE**] |
| **Data Format** | JPEG/PNG images, often resized to uniform dimensions (e.g., $256 \times 256$ or $512 \times 512$). |

**Data Note:** Data augmentation techniques (rotation, scaling, brightness adjustments) were heavily used to increase the model's robustness to real-world conditions.

## ⚙️ Model Architecture

The choice of architecture depends on the specific task:

### Option 1: Image Classification (If classifying the entire image)
* **Architecture:** ResNet50, MobileNetV2, or a custom CNN.
* **Method:** The model takes a cropped image of a single banknote and outputs the denomination class.

### Option 2: Object Detection (If localizing and classifying multiple banknotes)
* **Architecture:** YOLOv5, SSD (Single Shot Detector), or Faster R-CNN.
* **Method:** The model outputs bounding boxes around each detected banknote and assigns a denomination label to each box.

## 💻 Dependencies

To run this project, ensure you have a compatible Python environment and the following dependencies:

```bash
pip install tensorflow keras pandas numpy opencv-python Pillow [YOLO/PyTorch if using object detection]
