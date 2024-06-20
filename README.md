# COPD Detection from CT Scans
This repository contains a project for detecting <b>Chronic Obstructive Pulmonary Disease (COPD)</b> from <b>CT scan images</b> using deep learning techniques. The project leverages transfer learning and advanced neural network architectures to achieve high accuracy in classification.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Results](#results)

## Introduction
<b>Chronic Obstructive Pulmonary Disease (COPD)</b> is a progressive lung disease characterized by increasing breathlessness. Early detection of COPD through medical imaging, such as CT scans, is crucial for timely intervention and management. This project utilizes deep learning techniques to automatically detect the presence of COPD in CT scan images.

## Dataset
The dataset used in this project consists of CT scan images in DICOM format. The images were preprocessed and labeled for the presence or absence of COPD.

## Preprocessing
The DICOM images were preprocessed using the pydicom library to convert them into a suitable format for training the neural network. Key preprocessing steps included:
* Reading and converting DICOM images to numpy arrays.
* Normalizing pixel values.
* Resizing images to fit the input size requirements of the neural network.

## Model Architecture
Two different architectures were explored for this task:

<b>VGG16</b>: A pre-trained VGG16 model was initially used with fine-tuning. However, the model exhibited overfitting, suggesting that it was not the best fit for this dataset.

<b>Vision Transformer (ViT)</b>: The Vision Transformer, a state-of-the-art model for image classification, was then employed. This model provided better generalization and achieved higher accuracy on the test set.

## Training
The models were trained using transfer learning. Key steps included:

* Loading pre-trained weights.
* Fine-tuning the model on the CT scan dataset.
* Using data augmentation to enhance generalization.
* Monitoring training and validation loss to detect overfitting and adjust hyperparameters accordingly.

## Results
The Vision Transformer model achieved a test accuracy of <b>86.29%</b>, demonstrating its effectiveness in detecting COPD from CT scan images.
