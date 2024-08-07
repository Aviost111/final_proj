
#

---

## Overview

This repository contains a series of Jupyter notebooks designed to analyze coin classification models. The notebooks follow a structured process starting from data cleaning and preprocessing to feature extraction, model evaluation, and analysis of the model's behavior using masked images.

## Notebooks

1. **Data Cleaning and Preprocessing**: `01_Data_Cleaning_and_Preprocessing.ipynb`
2. **CNN Classification for Top Classes**: `02_CNN_Classification_Top_Classes.ipynb`
3. **Feature Extraction and Grad-CAM**: `03_Feature_Extraction_and_GradCAM.ipynb`
4. **Masked Coin Image Analysis with Grad-CAM**: `04_Masked_Coin_Image_Analysis_with_GradCAM.ipynb`

---

### 1. Data Cleaning and Preprocessing

**Notebook**: `01_Data_Cleaning_and_Preprocessing.ipynb`

**Description**:
This notebook handles the initial cleaning and preprocessing of the dataset.

**Key Steps**:

- Load raw image data and labels.
- Perform data cleaning (handling missing values, duplicates, etc.).
- Normalize image data.
- Create one image from two sides of the coin.
- Save cleaned data for subsequent analysis.

### 2. CNN Classification for Top Classes

**Notebook**: `02_CNN_Classification_Top_Classes.ipynb`

**Description**:
This notebook focuses on classifying the 2nd and 3rd largest classes in the dataset using Convolutional Neural Networks (CNNs).

**Key Steps**:

- Load cleaned data.
- Select the 2nd and 3rd largest classes.
- Split data into training, validation, and test sets.
- Train a CNN model.
- Evaluate model performance.

### 3. Feature Extraction and Grad-CAM

**Notebook**: `03_Feature_Extraction_and_GradCAM.ipynb`

**Description**:
This notebook focuses on extracting features from the images using a pre-trained model and applying Grad-CAM to visualize the regions of the images that the model focuses on during classification.

**Key Steps**:

- Load the pre-trained model.
- Perform feature extraction on the images.
- Apply Grad-CAM to visualize model focus areas.
- Save and display Grad-CAM results.

### 4. Masked Coin Image Analysis with Grad-CAM

**Notebook**: `04_Masked_Coin_Image_Analysis_with_GradCAM.ipynb`

**Description**:
This notebook investigates the robustness of the coin classification model by evaluating its performance on images with masked regions (both central and outer parts) focusing on the **two** largest classes. It also uses Grad-CAM to analyze the model's focus areas on these modified images.

**Key Steps**:

- Load and preprocess images.
- Mask the central or outer regions of the images.
- Evaluate the model's performance on masked images.
- Apply Grad-CAM to visualize model focus areas on masked images.
- Draw conclusions about the model's reliance on specific image features.

#### 5. Third Class Evaluation

**Notebook**: `05_Third_Class_Evaluation.ipynb`

**Description**:
This notebook tests the third largest class using the model trained only on the two largest classes to understand if the third class is similar to one of the largest classes and if its classification is consistent.

**Key Steps**:

- Load the model trained on the two largest classes.
- Load and preprocess images from the third largest class.
- Evaluate the model's performance on the third class.
- Analyze the consistency of the classification results.

---
