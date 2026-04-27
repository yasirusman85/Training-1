Alzheimer's Disease Classification using DenseNet121
Project Overview
This project implements a deep learning model to classify MRI images into four categories of Alzheimer's Disease: Mild Demented, Moderate Demented, Non-Demented, and Very Mild Demented.

Dataset
Source: Kaggle (preetpalsingh25/alzheimers-dataset-4-class-of-images)
Preprocessing:
Handled class imbalance by balancing all categories to ~1,000 images using data augmentation (rotation, shifting, shearing, zooming, and flipping).
Resized images to 224x224 pixels.
Normalized pixel values to the [0, 1] range.
Model Architecture
Base Model: DenseNet121 (Pre-trained on ImageNet)
Layers:
Frozen convolutional base to preserve feature extraction.
Global Average Pooling layer.
Dense layer (256 units, ReLU activation).
Dropout layer (0.5) for regularization.
Softmax output layer (4 classes).
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Training Results
Epochs: 10
Final Training Accuracy: ~65.2%
Final Validation Accuracy: ~62.9%
Conclusion
The model demonstrates a stable learning curve with minimal overfitting between training and validation sets. Further improvements could involve unfreezing the base model for fine-tuning or increasing the number of training epochs.
