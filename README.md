# Leaf Classification

## Overview

This project aims to predict leaf classification using neural networks based on features extracted from images of plant leaves. The primary objective is to accurately identify 99 species of plants using shape, margin, and texture features. This README provides an overview of the project, including its objectives, challenges, data description, project pipeline, and results.

## Project Details

Leaf Classification uses neural networks to identify plant species from leaf images. With optimized models, it achieves 99.49% validation accuracy, aiding botanical research.

- **Author:** Yara Elzahy
- **ID:** 20398570

### Problem Statement

Classification of plant species based on leaf features has historically been challenging, often leading to duplicate identifications. This project aims to address this issue by using deep learning techniques to accurately classify plant species based on binary leaf images and extracted features.

### Objectives

The main objectives of this project are:
- Utilize binary leaf images and extracted features to identify 99 species of plants.
- Address challenges such as missing data, unnecessary columns, and label encoding.
- Optimize hyperparameters to enhance model performance.

### Challenges

The challenges encountered in this project include:
1. Handling missing values (NaN cells).
2. Identifying and removing unnecessary columns.
3. Converting string labels to numerical values.
4. Selecting the best hyperparameters for neural network training.

### Impact

Successfully predicting the species of a leaf can significantly impact plant classification accuracy, aiding in botanical research and biodiversity conservation efforts.

## Data Description

The dataset comprises approximately 1,584 images of leaf specimens, each representing 16 samples of 99 plant species. Features extracted from these images include shape, margin, and texture descriptors, each represented by a 64-attribute vector per leaf sample. The dataset also contains an anonymous ID unique to each image.

### Data Fields

- **id:** Unique identifier for each image.
- **margin_1 to margin_64:** Attributes representing the margin feature.
- **shape_1 to shape_64:** Attributes representing the shape feature.
- **texture_1 to texture_64:** Attributes representing the texture feature.

## Project Pipeline

The project pipeline involves the following steps:

1. **Data Preparation:** Read, explore, visualize, clean, and preprocess the data.
2. **Training a Neural Network:** Build, train, evaluate, and optimize neural network models.

## Results

After training and evaluating various models with different hyperparameters, the following results were obtained:

- **Default Hyperparameters:**
  - Loss: 0.0021, Accuracy: 1.0000
  - Validation Loss: 0.0373, Validation Accuracy: 0.9848

- **Experimented Hyperparameters:**
  - Batch Size = 30: Validation Accuracy improved to 0.9949.
  - Dropout = 0.2: Validation Accuracy improved to 0.9949.
  - Optimizer = RMSprop: Validation Accuracy improved to 0.9949.
  - Hidden Layer = 180: Validation Accuracy improved to 0.9949.

- **Optimal Hyperparameters:**
  - Hidden Layer = 180
  - Optimizer = RMSprop
  - Dropout = 0.2
  - Batch Size = 30
  - Resulting Validation Accuracy: 0.9949

Finally, a comparison was made using the talos library for hyperparameter tuning, indicating that the trivial approach outperformed the fine-tuned one.

## Conclusion

The project successfully demonstrates the use of neural networks for leaf classification, achieving high accuracy in identifying plant species based on extracted features. Further optimization using grid search techniques may provide insights for future improvements.
