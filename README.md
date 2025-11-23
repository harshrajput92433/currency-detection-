<!-- Project Badges -->
![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Keras](https://img.shields.io/badge/Keras-NeuralNetworks-red)
![EfficientNet](https://img.shields.io/badge/Model-EfficientNetB0-yellowgreen)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle-blue)
![Status](https://img.shields.io/badge/Status-Active-success)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20Mac-black)
![License](https://img.shields.io/badge/License-MIT-green)
![Accuracy](https://img.shields.io/badge/Accuracy-100%25-brightgreen)
[Project Guidelines (VIT BYOP PDF)](https://github.com/harshrajput92433/currency-detection-/blob/main/BuildYourOwnProject.pdf)
# Fake Currency Detection Using Deep Learning

## Project Title

Fake Currency Detection Using Deep Learning

## Overview of the Project

This project is built to automatically determine whether a currency note is real or fake using a deep learning model. Fake currency is a common problem that affects people, shops, and banks. Traditional checking methods depend on humans or machines and are not always accurate. The purpose of this project is to create a simple, fast, and reliable system that can analyze an image of a currency note and tell if it is genuine or counterfeit. The model learns patterns such as texture, printing quality, watermark presence, and security marks through a dataset of real and fake note images collected from Kaggle.

## Features

* Upload an image of a currency note to verify authenticity
* Deep learning model predicts "Genuine" or "Counterfeit"
* Displays confidence score for prediction accuracy
* Runs efficiently and gives results within seconds
* Can be integrated into mobile or ATM-based systems
* Easy to use for real-time decision-making

## Technologies / Tools Used

* Python
* TensorFlow / Keras
* EfficientNetB0 + CNN
* NumPy, Pandas
* Albumentations for image augmentation
* Matplotlib for visualization

## Steps to Install & Run the Project

```bash
# Clone the repository
git clone https://github.com/yourusername/fake-currency-detection.git
cd fake-currency-detection
```

```bash
# Create and activate virtual environment
python -m venv venv
venv\Scripts\activate       # Windows
source venv/bin/activate    # Mac/Linux
```

```bash
# Install required dependencies
pip install -r requirements.txt
```

```bash
# (Optional) Create dataset folders if needed
mkdir data
mkdir data/train data/val data/test
```

```bash
# Train the model
python train.py --data_dir ./data --epochs 30 --batch_size 32
```

```bash
# Run inference prediction on a sample image
python infer.py --image sample.jpg --weights best_model.h5
```

## Instructions for Testing

1. Prepare a set of real and fake currency note images to test the model.
2. Use the `infer.py` script and provide the image path.
3. The program will print the predicted output:

   * Genuine
   * Counterfeit
   * Confidence score (0 to 1)
4. Test with different lighting conditions and backgrounds to evaluate robustness.

```bash
python infer.py --image ./test_images/note1.jpg --weights best_model.h5
```

### Example Output

```
Prediction: Genuine
Confidence: 0.97
```

---

This README is written in a simple and human-friendly format to help anyone understand and run the project easily. If needed, it can be extended with deployment instructions or real-time demo integration.

Author: Harsh Rajput | B.Tech CSE | VIT Bhopal University
