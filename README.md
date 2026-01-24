# **Kurdish Sign Language Recognition (KuSL2023) – Research Paper Implementation**

## **Overview**
This repository contains the Python and Jupyter Notebook (`.ipynb`) code developed as part of the implementation of the research paper **“KuSL2023: A CNN-Based Recognition Method for Kurdish Sign Language Detection and Classification.”**

The project focuses on recognizing **static Kurdish Sign Language (KuSL) alphabet hand gestures** using computer vision and machine learning techniques.  
This repository is intended to demonstrate the **methodology, preprocessing pipeline, and model implementation**, rather than providing trained models or datasets.

---

## **Research Paper Reference**
**KuSL2023: A CNN-Based Recognition Method for Kurdish Sign Language Detection and Classification**  
Published in *MethodsX, Elsevier (2025)*

The code in this repository follows the workflow, preprocessing steps, and evaluation strategy described in the paper.

---

## **Dataset Information**
- Dataset Name: Kurdish Sign Language Dataset (KuSL2023)
- Total Images: 71,400
- Number of Classes: 34 Kurdish alphabet signs
- Image Types: RGB and Grayscale
- Gesture Type: Static hand gestures

The dataset is **not included** in this repository.  
It is publicly available online via **Mendeley Data**, as referenced in the original research paper.

---

## **Models Implemented**
The following models are implemented in the code:

- Convolutional Neural Network (CNN)  
  - Framework: TensorFlow / Keras  
  - Input Size: 64 x 64 RGB images  

- K-Nearest Neighbors (KNN)  
  - Trained on flattened grayscale image features  

- Logistic Regression (LR)  
  - Trained on grayscale image vectors  

Model training and evaluation are performed within Jupyter notebooks and Python scripts.

---

## **Preprocessing Pipeline**
- Image resizing to 64 x 64
- Pixel normalization
- RGB images used for CNN
- Grayscale images flattened for traditional machine learning models
- Label encoding and stratified train-test split

---

## **Repository Contents**
Included:
- Jupyter Notebook files (`.ipynb`)
- Python source code files (`.py`)

Not Included:
- Dataset files
- Trained model files
- Image data

---

## **How to Use**
1. Download the KuSL2023 dataset from the official online source.
2. Place the dataset in the expected directory structure.
3. Run the Jupyter notebooks or Python scripts to preprocess data, train models, and evaluate performance.
4. Modify or extend the code for further experimentation.

---

## **Applications**
- Kurdish Sign Language recognition
- Assistive technologies for the hearing-impaired
- Gesture recognition systems
- Machine learning and computer vision research

---

## **Disclaimer**
This repository is intended for educational and research purposes only.  
All credit for dataset creation and original methodology belongs to the authors of the KuSL2023 research paper.
