# MRI Brain Tumor Detection with EfficientNet

This project demonstrates a deep learning approach for detecting brain tumors from MRI images using EfficientNet architectures.

## Overview

- **Dataset:** Brain MRI images labeled as 'tumor' and 'no tumor' (downloaded from [Kaggle](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection))
- **Models:** EfficientNet-B0 and EfficientNet-B3 (with progressive training)
- **Frameworks:** PyTorch, torchvision, timm

## Workflow

1. **Data Preparation**
   - Download the MRI dataset from Kaggle using your API token.
   - Unzip and organize images by class: “yes” (tumor) and “no” (no tumor).
   - Explore and visualize sample images and class distribution.

2. **Preprocessing and Augmentation**
   - Apply data augmentation techniques (random crop, flips, rotations, color jitter, erasing) to bolster the training set.
   - Normalize data based on ImageNet statistics.
   - Create PyTorch Dataset and DataLoader objects for train, validation, and test partitions.

3. **Model Setup**
   - Define EfficientNet architectures (B0 and B3).
   - Modify the classification layer for binary output.
   - Configure hyperparameters: learning rate, batch size, dropout, optimizer, early stopping.

4. **Training**
   - Train EfficientNet-B0 with aggressive augmentation.
   - Train EfficientNet-B3 in two stages: first, train only the classifier layer; then fine-tune the whole model.
   - Monitor metrics (loss, accuracy) for both train and validation data.
   - Use callbacks like early stopping and learning rate schedulers.

5. **Evaluation**
   - Assess model performance on the test set.
   - Compute metrics: accuracy, confusion matrix, precision, recall, F1-score, ROC curves.
   - Visualize performance and analyze model predictions.

6. **Saving and Loading Models**
   - Save the best-performing model weights for inference and further experiments.
   - Demonstrate how to reload models and run predictions on new MRI images.

---

This workflow allows you to train, validate, and deploy deep learning models for brain tumor MRI image classification efficiently.

## Reference

- [Kaggle Dataset: Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)
