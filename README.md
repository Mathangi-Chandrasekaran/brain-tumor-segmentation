# Brain Tumor Segmentation Using U-Net and Attention U-Net

A deep learning project exploring pixel-level brain tumor segmentation from MRI images using U-Net and Attention U-Net. The project compares a baseline encoder–decoder architecture with an attention-enhanced model to investigate their ability to identify tumor regions.

## Overview
Accurate brain tumor segmentation can help researchers analyze tumor boundaries, shape and size in medical images. Manual segmentation can be time-consuming and requires specialist expertise.

This project implements and compares two convolutional neural network architectures:

* U-Net: An encoder–decoder network with skip connections for spatial localization and image segmentation.

* Attention U-Net: An extension that uses attention gates to emphasize relevant image features and suppress less relevant background information.

The objective is to evaluate whether incorporating attention improves segmentation performance compared with the baseline U-Net.

## Dataset

The project uses a publicly available Brain MRI Segmentation dataset from Kaggle, described in the report as containing MRI scans from 110 patients with lower-grade gliomas and manually annotated FLAIR abnormality segmentation masks.

The report describes combining three MRI modalities into RGB images and pairing each image with its corresponding segmentation mask.

The dataset is used to train and evaluate models that predict tumor regions at the pixel level.

## Evaluation

The models are evaluated using multiple segmentation metrics:

Dice Coefficient: Measures overlap between predicted and ground-truth tumor regions.

Intersection over Union (IoU): Measures the intersection relative to the union of the two regions.

Sensitivity (Recall): Measures the proportion of actual tumor pixels correctly identified.

Specificity: Measures the proportion of background pixels correctly identified.

Pixel Accuracy: Measures the proportion of all pixels classified correctly.

Loss curves: Help inspect training behaviour and potential overfitting.

## Limitations and Future Work

The project report identifies several limitations and opportunities for improvement:
Class imbalance between tumor and non-tumor regions.
Computational and memory constraints during training and hyperparameter optimization.
Potential overfitting, which requires careful validation.
Further exploration of data augmentation and sampling strategies.
Interactive visualizations for examining segmentation outputs.


**Disclaimer:**

This project is intended for research and educational purposes only. The reported metrics do not establish clinical validity, and the models should not be used for diagnosis or treatment decisions.

