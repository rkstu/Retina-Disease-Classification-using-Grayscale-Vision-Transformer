# Retina Disease Classification Using a Grayscale Vision Transformer

This repository contains the implementation of a custom Vision Transformer (ViT) model for classifying retinal diseases using grayscale OCT images. The model is designed for accuracy, interpretability, and computational efficiency, making it suitable for potential clinical applications.

## Overview

The project focuses on differentiating four retinal conditions using high-resolution OCT scans. A modified ViT architecture is used to capture long-range dependencies in retinal structures and generate interpretable attention maps. The model achieves competitive performance while maintaining a relatively compact parameter size.

## Key Features

* Custom Vision Transformer architecture adapted for grayscale medical imaging
* High accuracy on the SD-OCT dataset with strong specificity and sensitivity
* Improved interpretability through attention-based heatmaps
* Efficient parameter configuration (approximately 44.4 million parameters)
* Standardized preprocessing pipeline for consistent training

## Dataset

The model is trained on the publicly available Labeled OCT Dataset containing 84,495 images across four classes:

* CNV
* DME
* DRUSEN
* NORMAL

Dataset source:
[https://data.mendeley.com/datasets/rscbjbr9sj/2](https://data.mendeley.com/datasets/rscbjbr9sj/2)

## Model Architecture

* Input image size: 384 x 384
* Input channels: 1 (grayscale)
* Transformer layers: 24
* Embedding dimension: 256
* Attention heads: 16
* Number of classes: 4

## Training Details

* Loss function: Cross Entropy with label smoothing
* Optimizer: Adamax with a learning rate of 0.0002
* Batch size: 18
* Epochs: 10
* Preprocessing steps:

  * Grayscale conversion
  * Resize to 384 x 384 using bicubic interpolation
  * Center crop
  * Tensor conversion
  * Normalization using mean 0.485 and standard deviation 0.229

## Evaluation Metrics

The model is evaluated using the following metrics:

* Accuracy
* Precision
* Recall (Sensitivity)
* Specificity

Performance of the ViT (Ours) model:

* Accuracy: 97.30 percent
* Specificity: 98.975 percent
* Precision: 97.35 percent
* Recall: 97.30 percent


## Resources

Project repository:
[https://github.com/rkstu/Retina-Disease-Classification-using-Grayscale-Vision-Transformer.git](https://github.com/rkstu/Retina-Disease-Classification-using-Grayscale-Vision-Transformer.git)

Dataset:
[https://data.mendeley.com/datasets/rscbjbr9sj/2](https://data.mendeley.com/datasets/rscbjbr9sj/2)

