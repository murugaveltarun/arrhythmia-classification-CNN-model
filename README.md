# ECG Signal Classification Project


## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
---

## Introduction

This project uses the MIT-BIH Arrhythmia dataset to classify ECG signals into five groups: normal and four types of irregular heartbeats. The input data is first preprocessed, and the classes are rebalanced to ensure fair training. A Convolutional Neural Network (CNN) is then used to extract features and classify the signals. The model includes layers for feature detection, data reduction, and overfitting prevention, ending with a softmax layer for classification. It is tested and evaluated with high accuracy, demonstrating its effectiveness in identifying different irregular ECG patterns with respect to their classes.

---

## Dataset

### MIT-BIH Arrhythmia Database:
- Includes ECG signals from 48 subjects.
- Contains annotated examples of various arrhythmias.
- The dataset is publicly available on [PhysioNet](https://physionet.org/physiobank/database/mitdb/) and [Kaggle](https://www.kaggle.com/datasets/taejoongyoon/mitbit-arrhythmia-database).

#### Preprocessing Steps:
- **Data extraction and denoising:** Here, the bandpass filter is used to extract only the ECG data and remove noise. Z-score normalization is applied to minimize the scale, and finally, the QRS complex is extracted as a single sample.

- **Class rebalancing to handle imbalances in arrhythmia types:** Class balancing is performed to ensure equal learning for all classes, which helps to avoid overfitting.

- **Train-test split :**  The dataset is divided into training and testing sets in an 80:20 ratio.

---

## Methodology

### CNN Architecture:
The model comprises:
1. **Convolutional Layers**: To extract meaningful features.
2. **Pooling Layers**: To reduce dimensionality while preserving essential information.
3. **Fully Connected Layers**: To make predictions based on learned features.

### Workflow:
1. Data preprocessing and class rebalancing.
2. Train-test split.
3. Model training.
4. Evaluation on unseen data (testing data).

![block diagram (or) workflow](https://github.com/murugaveltarun/arrhythmia-classification-CNN-model/blob/5eba2d5d4313f5f5003bce8b75970c5188ae1cab/block.png)

---

## Results

This model achieved a 99.32% validation accuracy.

![results](https://github.com/murugaveltarun/arrhythmia-classification-CNN-model/blob/5eba2d5d4313f5f5003bce8b75970c5188ae1cab/res.png)
