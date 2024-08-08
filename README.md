
#

---

## Overview

This repository contains a series of Jupyter notebooks designed to analyze coin classification models. The notebooks follow a structured process starting from data cleaning and preprocessing to feature extraction, model evaluation, and analysis of the model's behavior using masked images.

## Notebooks

0. **Organize Data into Folders**: `00_Organize_Data_To_Folders.ipynb`
1. **Data Cleaning and Preprocessing**: `01_Data_Cleaning_and_Preprocessing.ipynb`
2. **CNN Classification for Top Classes**: `02_CNN_Classification_Top_Classes.ipynb`
3. **Feature Extraction and Grad-CAM**: `03_Feature_Extraction_and_GradCAM.ipynb`
4. **Masked Coin Image Analysis with Grad-CAM**: `04_Masked_Coin_Image_Analysis_with_GradCAM.ipynb`
5. **Third Class Evaluation**: `05_Third_Class_Evaluation.ipynb`
6. **Three Class Model Training and Analysis**: `06_Three_Class_Model_Training_and_Analysis.ipynb`

---

### 0. Organize Data into Folders

**Notebook**: `00_Organize_Data_To_Folders.ipynb`

**Description**:
This notebook organizes the combined coin images into separate folders based on their class labels. It also renames the images to include their class labels.

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

### 5. Third Class Evaluation

**Notebook**: `05_Third_Class_Evaluation.ipynb`

**Description**:
In this notebook, we evaluate the robustness of our pre-trained coin classification model by testing it on images from a third class, al-Mahdiyah, which was not part of the original training set. The goal is to understand if the al-Mahdiyah class shares similarities with the two largest classes (Misr and al-Mansuriyah) used in the initial training.

**Key Steps**:

- Load and preprocess images of the al-Mahdiyah class.
- Use the pre-trained model to predict the class of al-Mahdiyah images and analyze the classification consistency.
- Apply Grad-CAM to visualize the regions of the al-Mahdiyah images that the model focuses on when making its predictions.
- Draw conclusions about the model's reliance on specific image features.

### 06. Three Class Model Training and Analysis

**Notebook**: `06_Three_Class_Model_Training_and_Analysis.ipynb`

**Description**:
In this notebook, we extend our previous work by training a convolutional neural network (CNN) to classify coins from three mints: `al-Mansuriyah`, `Misr`, and `al-Mahdiyah`. We analyze the model's performance and conduct various experiments to understand the importance of different coin regions in classification.

**Key Steps**:

- Organize and preprocess images from the three classes.
- Split the dataset into training, validation, and test sets.
- Define and compile a CNN model.
- Train the model on the three-class dataset.
- Evaluate the model's performance on the test set.
- Apply Grad-CAM to visualize important regions in the images.
- Modify images by masking specific regions and evaluate the model.
- Use Grad-CAM on modified images to understand feature importance.

---
