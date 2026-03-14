Kurdish Sign Language Recognition using Deep Learning
Overview

This project focuses on building an AI system that recognizes Kurdish Sign Language gestures using deep learning. The goal is to classify hand gesture images into 34 different Kurdish sign language classes using modern computer vision models.

To achieve this, multiple deep learning architectures were implemented and compared, including:

Custom Convolutional Neural Network (CNN)

ResNet50 (Transfer Learning)

EfficientNet-B0

Vision Transformer (ViT)

Hybrid Feature Fusion Model (ResNet + ViT)

The final hybrid model achieved 99.31% classification accuracy on the validation dataset.

Dataset

The model was trained on the KuSL2023 Kurdish Sign Language Dataset, which contains:

71,000+ labeled images

34 gesture classes

RGB hand gesture images

Each class corresponds to a unique Kurdish sign language symbol.

Images were resized and normalized before training to ensure consistent input across models.

Project Pipeline

The project followed a progressive deep learning workflow:

Build a baseline CNN model

Apply transfer learning with ResNet50

Train EfficientNet for efficient CNN architecture

Implement Vision Transformer (ViT)

Combine CNN and Transformer features using a fusion model

This pipeline allows comparison between traditional CNN models and transformer-based architectures.

Model Architectures
1. Custom CNN (Baseline)

A simple convolutional neural network was built from scratch with:

Convolution layers

Max pooling

Fully connected layers

Dropout regularization

This served as the baseline model.

Accuracy achieved:

96.6%

2. ResNet50 (Transfer Learning)

A pretrained ResNet50 model was used with ImageNet weights.

Steps:

Freeze backbone layers

Replace classifier layer

Fine-tune final blocks

Accuracy achieved:

99.2%

3. EfficientNet-B0

EfficientNet uses compound scaling to balance depth, width, and resolution.

Steps:

Load pretrained EfficientNet-B0

Train classifier head

Fine-tune deeper layers

Accuracy achieved:

98.2%

4. Vision Transformer (ViT-Small)

A transformer-based vision model was trained using ViT-Small.

Unlike CNNs, transformers process images as patch sequences and learn global relationships using self-attention.

Accuracy achieved:

98.54%

5. Feature Fusion Model (ResNet + ViT)

The final model combines features from:

ResNet50 (spatial CNN features)

Vision Transformer (global attention features)

Architecture:

Image
 ├── ResNet50 → Feature Vector
 ├── ViT-Small → Feature Vector
 └── Concatenation → Fusion Network → Classifier

The fusion network learns to combine both feature types for improved representation.

Final accuracy achieved:

99.31%

Model Performance Comparison
Model	Accuracy
Custom CNN	96.6%
ResNet50	99.2%
EfficientNet-B0	98.2%
ViT-Small	98.54%
Fusion Model (ResNet + ViT)	99.31%

The fusion architecture achieved the best performance.

Evaluation Metrics

The final model was evaluated using:

Accuracy

Precision

Recall

F1-score

Confusion Matrix

Example confusion matrix:

(Add confusion_matrix.png here)

The evaluation report was generated using scikit-learn classification metrics.

Technologies Used

Python

PyTorch

TorchVision

TIMM (Vision Transformer models)

NumPy

Scikit-learn

Matplotlib

Seaborn

Project Structure
kurdish-sign-language-recognition
│
├── notebooks
│   ├── cnn_training.ipynb
│   ├── resnet_training.ipynb
│   ├── efficientnet_training.ipynb
│   ├── vit_training.ipynb
│   └── fusion_model.ipynb
│
├── models
│   └── fusion_model_final.pth
│
├── results
│   ├── evaluation_report.txt
│   └── confusion_matrix.png
│
├── requirements.txt
└── README.md
Installation

Clone the repository:

git clone https://github.com/yourusername/kurdish-sign-language-recognition.git
cd kurdish-sign-language-recognition

Install dependencies:

pip install -r requirements.txt
Future Improvements

Possible improvements include:

Real-time gesture recognition using webcam

Deploying the model as a web application

Building a mobile sign language translator

Expanding the dataset to include more gestures

Author

Developed by Kavya Dari

Computer Science Student | Machine Learning Enthusiast