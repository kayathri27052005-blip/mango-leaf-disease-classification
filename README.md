# Mango Leaf Disease Classification using EfficientNetB0

## Project Overview

This project uses deep learning and transfer learning to classify mango leaf images into eight different categories.

The model is designed to identify mango leaf diseases from images and distinguish them from healthy leaves.

## Classes

The model classifies images into 8 classes:

- Anthracnose
- Bacterial Canker
- Cutting Weevil
- Die Back
- Gall Midge
- Healthy
- Powdery Mildew
- Sooty Mould

## Dataset

A cleaned dataset containing 4,000 original images was used.

The dataset was divided using a stratified split:

- Training: 70% - 2,800 images
- Validation: 15% - 600 images
- Testing: 15% - 600 images

Artificially generated augmented copies were removed before splitting the dataset to reduce the risk of data leakage.

## Model

EfficientNetB0 was used with ImageNet pretrained weights.

Architecture:

Input Image
↓
Image Augmentation
↓
EfficientNetB0
↓
Global Average Pooling
↓
Dropout
↓
Dense Layer
↓
Softmax
↓
8 Classes

## Data Augmentation

Training images were augmented using:

- Random horizontal flipping
- Random rotation
- Random zoom
- Random contrast

Augmentation was applied only during training.

## Training

Frameworks and libraries:

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

Optimizer:

Adam

Loss function:

Sparse Categorical Cross-Entropy

## Results

Validation Accuracy: 99.83%

Test Accuracy: 99.67%

Test Set: 600 images

The model correctly classified 598 out of 600 test images.

## Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Prediction

The trained model can be used to predict the disease class of a new mango leaf image and provide the predicted class with its confidence score.

## Future Improvements

- Test with more real-world field images
- Improve robustness to different lighting and backgrounds
- Deploy the model as a web or mobile application
- Expand the dataset with images from different regions

## Author

Gayathri B
