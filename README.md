<div align="center">

# Leg Bone Segmentation with AI | Python, Labelme, Model
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)<br>


</div>

## What Is This Leg Bone Segmentation with AI ? 🤔

This is an AI-based system for leg bone segmentation from X-ray images using advanced preprocessing, feature extraction (HOG, CoHOG, LBP, Sobel), and cross-correlation techniques. Achieved IoU of 0.7137. Completed in Spring Term, 2024–2025.

## Preview

- Here is a little part of the model.


<div align="center" style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; max-width: 420px; margin: auto;">
  <img src="https://i.imgur.com/XlfzJzp.png" alt="Image 1" style="width: 200px; aspect-ratio: 1 / 1; object-fit: cover;">
</div>


## Used Technologies
HOG (Histogram of Oriented Gradients): Extracted edge-based features for image analysis.

CoHOG (Co-occurrence of HOG): Captured spatial relationships between gradient patterns.

LBP (Local Binary Pattern): Used for local texture feature extraction.

Cross-Correlation & Fast Cross-Correlation: Applied for similarity measurement between images and label regions.

Patch Extraction: Divided images into smaller sections for localized processing.

Gradient Orientation & Sobel Operator: Computed edge directions and magnitudes.

Brightness Adjustment & Sharpening: Image enhancement techniques used during preprocessing.

Mean & L1 Norm: Used for image normalization and statistical consistency.

Pyramid Representation: Multi-scale image processing technique.

Shannon Entropy: Used as an information metric to evaluate preprocessing pipelines.

IOU (Intersection over Union): Evaluated the accuracy of predicted regions against ground truth.

Boundary Detection & Label Edge Evaluation: Assessed alignment of boundaries between label and prediction.

LabelMe Annotation Tool: Employed for manual labeling of dataset.

PyTorch & MONAI Frameworks: Used to build and train AI models for medical image analysis.

Adam Optimizer: Adaptive optimization method used during training.

Epoch-Based Learning: Iterative training over multiple cycles to optimize model accuracy.

Artificial Intelligence Model Training: Built and evaluated models using handcrafted features.

## Preprocessing Pipeline Performance (Shannon Entropy Based)
Pipeline 1: L1 Norm + Median + Histogram Equalization → Entropy = 5.6044

Pipeline 2: L1 Norm + Median + Brightness(+20) → Entropy = 5.8738

Pipeline 3: L1 Norm + Median + Contrast Enhancement → Entropy = 5.2499

Pipeline 4: L2 Norm + Adaptive Median + Brightness(+50) → Entropy = 5.8738

Pipeline 5: L1 Norm + Mean + Brightness(+20) → Entropy = 5.8738

Pipeline 6: L1 Norm + Mean + Brightness(+20) + Sharpening → Entropy = 5.9376

Pipeline 7: L1 Norm + Sharpening + Mean + Brightness(+20) → Entropy = 5.9376

Best Pipeline (Shannon Entropy):

Pipeline 6 → Entropy = 5.9376

##Edge Pattern Coding Final IoU Evaluation (Cross-Correlation Based)

(4_1) Boundary + Image Edge Lines + HOG + Sobel Points + Cross-Correlation → Final IoU = 0.7020

(4_2) Boundary + Image Edge Lines + Single HOG + Sobel Points + Cross-Correlation → Final IoU = 0.7137

(4_3) Image + Label + Boundary + HOG + Cross-Correlation → Final IoU = 0.6477

(4_4) Label Edge (k-radius) + Boundary + HOG + Cross-Correlation → Final IoU = 0.6185

(4_5 - Sobel Test) Label Edge (k-radius) + Boundary + HOG + Sobel-HOG + Cross-Correlation → Final IoU = 0.6302

Best IoU Result:

(4_2) Method → IoU = 0.7137


