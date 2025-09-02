# Deepfake-Detection-with-XAI
This project implements a deepfake detection system using deep learning (ResNet34) combined with explainability techniques to improve model transparency. The goal is to distinguish between real and fake face images with high accuracy and provide visual explanations for the model’s predictions.
Project Overview

Deepfakes pose a serious threat to digital media authenticity. In this project, we trained a ResNet34-based image classifier to detect fake vs. real face images and integrated post-hoc explainability to understand which regions in the image contributed most to the classification.

Key Features:

Binary classification: Real vs. Fake images
Explainability: GradCAM, LIME and IG visualizations
Evaluation through confusion matrix, ROC curve, and training plots
Model Architecture

Base model: ResNet34 (pretrained on ImageNet, fine-tuned for binary classification)
Explainability tools: GradCAM, LIME and IG
Results

Accuracy Achieved: 99.21%
Strong performance on validation and test sets
Visual analysis included: ROC curve, confusion matrix, dataset distribution, and training metrics
Output & Evaluation

All key evaluation metrics and plots (including training history, ROC curve, confusion matrix, and dataset distribution) are provided in the results/ folder.
Sample output images for explainability techniques — GradCAM, LIME, and Integrated Gradients (IG) — are also included in the results/ folder for reference.
These examples help you understand how the model interprets and distinguishes between real and fake images.
How to Use

You can easily run this project using Google Colab by following these steps:

Open the Notebook
Import the provided .py notebook into your Google Colab environment.
Upload the Dataset (Kaggle) This project uses the "140k Real and Fake Faces" dataset from Kaggle.

Download your Kaggle API key as a kaggle.json file from your Kaggle account.
Upload kaggle.json in the first cell to authenticate and automatically download the dataset.
Run the Notebook

Execute all cells sequentially to load the dataset, train the model, evaluate it, and generate visual explanations using GradCAM, LIME, and Integrated Gradients.
Test on Custom Images

You can upload any face image and test whether it’s detected as real or fake.
The notebook provides visual explanations highlighting which parts of the image influenced the model’s prediction.

Tip: Enable a T4 GPU in Colab (under Runtime > Change runtime type > Hardware accelerator > GPU) for significantly faster training. Training on CPU will be much slower and is not recommended for full-scale runs.
