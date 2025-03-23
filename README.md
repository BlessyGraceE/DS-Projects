# Retinal Image Analysis for Early CANCER RISK PREDICTION

Introduction:

Overview:
Cancer risk prediction using retinal imaging is an emerging field that explores the correlation between retinal biomarkers and systemic diseases, including cancer. This project leverages deep learning techniques to analyze retinal images and brain MRI scans to predict cancer risk.

Objectives:
Classify retinal diseases using deep learning.
Classify brain tumors using MRI scans.
Develop a relationship logic for cancer risk prediction.
Evaluate model performance and analyze key findings.

Steps involved:
STEP 1 : Data Preprocessing
1.1 Load and Organize Data
Dataset 2 (Retinal Diseases - Normal, Cataract, Glaucoma, Diabetic Retinopathy): Organize into labeled classes.
Dataset 3 (Brain Tumour MRI Dataset): Separate training and testing images.

1.2 Data Augmentation (if needed)
Apply augmentation techniques to enhance model robustness:  Rotation, flipping, brightness adjustments, normalization,etc

1.3 Preprocess Images
Resize images to a fixed dimension (e.g., 224×224 for CNN input).
Normalize pixel values (scale between 0-1 or -1 to 1).

STEP 2 : Build the Deep Learning Models

2.1 Retinal Disease Classification Model
CNN or Transfer Learning (MobileNetV2)
Train on Dataset 1 (retinal images) to classify eye diseases.

2.2 Brain Tumour Classification Model
CNN or Pretrained Model (MobileNetV2)
Train on Dataset 3 (brain MRI) for tumour classification

STEP 3: Model Training & Evaluation

Use Adam optimizer, categorical cross-entropy (for multi-class classification).
Train each model separately with 10 epochs
Evaluate using accuracy, precision, recall and F1-score

STEP 4: CANCER RISK PREDICTION
Retinal prediction model classifies images into four classes: Normal - 0, Cataract – 1, Diabetic Retinopathy – 2, Glaucoma – 3
Brain prediction model classifies images into four classes: No tumour – 0, Glioma – 1, Meningioma – 2, Pituitary – 3

Cancer risk prediction logic:
High risk : If the retinal image is classifies as a disease (1, 2 or 3) and the brain image shows a tumour (1,2 or 3).
Moderate risk : If the retinal image has a disease (1, 2 or 3) but no brain tumour (0)
Monitor closely : If the retinal image is normal (0) but a brain tumour is present (1, 2, or 3).
﻿Low Risk: If both the retinal and brain images are classified as normal (0)

Datasets Used:

 Retinal Disease Dataset
Consists of four classes: Cataract, Glaucoma, Diabetic Retinopathy, and Normal.
Images are preprocessed and split into training (80%), validation (10%) and training (10%)

Brain MRI Dataset
Contains MRI scans categorized into four classes: Glioma, Meningioma, No Tumor, and Pituitary.
 Split into training and testing sets

Conclusion:

Retinal image analysis represents a promising, non-invasive method for the early detection of brain tumours. 
With advancements in AI and imaging technologies, this approach could complement existing diagnostic methods, enabling earlier intervention and improved patient outcomes. 
Further research and clinical validation are necessary to establish its role in routine medical practice. For beginners in deep learning and machine learning, understanding the fundamental steps of data pre-processing, model selection, and evaluation is crucial for contributing to this field.
Future work includes integrating clinical metadata for better accuracy