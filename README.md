# Dark Matter Substructure Classification

## Overview
This repository contains the code and resources for the final project in the PH451 Machine Learning course. The project aims to replicate the results from the ML4SCI DeepLense project by classifying different types of dark matter using simulated strong lensing images through deep learning techniques.

## Abstract
The goal of this project is to classify dark matter substructures using simulated strong lensing images. We employed various deep learning frameworks, including Convolutional Neural Networks (CNNs) and Transformers, to analyze and compare their performance. Our results show that EfficientNet_B0 achieved the highest accuracy and AUC, while Lensformer demonstrated the lowest loss.

## Data Description
The dataset comprises simulated strong lensing images generated using the `lenstronomy` Python library. These images are categorized into three classes: `no_sub` (no substructure), `cdm` (cold dark matter), and `axion` (axion dark matter). Each image is a single-channel NPY file of 64x64 pixels.

- **Train dataset size**: 80,457 images
- **Validation dataset size**: 8,939 images
- **Test dataset size**: 15,000 images

## Models and Methods
We evaluated several deep learning models:
- CNN
- ResNet18
- EfficientNet_B0
- Vision Transformer (ViT)
- Convolutional Transformer (CvT)
- Lensformer

Each model was trained for 100 epochs using Cross Entropy Loss and the Adam optimizer. The primary metric for evaluating the models' performance was the area-under-the-curve (AUC) metric.

## Results
After 100 epochs of training:
- **EfficientNet_B0**: Achieved the highest accuracy (99.17%) and AUC (0.9994).
- **Lensformer**: Had the lowest test loss (0.0446), indicating high stability.

All models performed exceptionally well, with AUC scores above 0.99. The CNN model was the most efficient in terms of training time.

## Conclusion
Deep learning techniques can effectively classify dark matter substructures with high accuracy. EfficientNet_B0 and Lensformer stood out due to their performance and stability. However, the models might face challenges when applied to real-world data due to the limitations of simulated datasets.

For more information and the original project, please refer to [ML4SCI DeepLense](https://github.com/ML4SCI/DeepLense).
