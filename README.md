# Fruit and Vegetable Freshness Classification and Grading

## Overview
This project focuses on automated food quality assessment using machine learning techniques. It performs two major tasks:

1. **Classification**
   - Identifies the name of food 
   - Determines whether the food is **fresh or rotten**

2. **Freshness Grading**
   - Assigns a **freshness score (0–100)** using multiple analytical methods

The system combines multiple machine learning models and grading techniques to improve accuracy and reliability.


## Objectives
- Classify food type
- Detect freshness (Fresh vs Rotten)
- Generate a numerical freshness score (0–100)
- Compare performance of multiple ML models
- Improve robustness using multi-metric grading


## Methodology

### A. Classification Models
The following machine learning models are used:

- **Support Vector Machine (SVM)**  
  Effective for high-dimensional feature spaces.

- **K-Nearest Neighbors (KNN)**  
  Classifies based on similarity with nearest data points.

- **Logistic Regression**  
  Probabilistic model for binary classification.

- **Random Forest**  
  Ensemble model that improves accuracy using multiple decision trees.

- **XGBoost**  
  Advanced boosting algorithm with high performance and efficiency.


### B. Freshness Grading Techniques

The freshness score (0–100) is calculated using multiple methods:

1. **Cosine Similarity**
   - Measures similarity between test sample and fresh reference features.

2. **Degradation Quality Index (DQI)**
   - Quantifies how much the sample deviates from ideal freshness.

3. **Distance-Based Method**
   - Uses distance (e.g., Euclidean) from fresh feature clusters.

4. **DASFS + KNN Anomaly Detection**
   - Dual-task feature selection combined with anomaly detection to identify degradation.

5. **Dual-Task Feature Selection with Reliability Gating**
   - Selects stable features and filters unreliable predictions.

6. **Cross-Feature Ratio DK Index**
   - Uses ratios between features to capture degradation patterns.


## Project Design

The project follows a **modular experimental approach**, where different components are implemented and evaluated independently rather than combined into a single pipeline.

- Multiple classification models are trained and tested independently  
- Multiple grading techniques are applied independently  

This design allows:
- Easy comparison of different models  
- Flexibility in selecting methods  
- Better understanding of performance trade-offs  


## Features Used

The system uses a total of **30 handcrafted features**:

R mean, G mean, B mean,  
R std, G std, B std,  

H mean, S mean, V mean,  
H std, S std, V std,  

L mean, L std, a mean, a std, b mean, b std,  

Laplacian variance,  
GLCM contrast, GLCM energy, GLCM homogeneity,  
grayscale entropy,  

contour area, perimeter, circularity, solidity, aspect ratio, extent,  

dark pixel ratio  


## Dataset

This project uses two public datasets:

Vegetable Dataset:  
  https://www.kaggle.com/datasets/user2036/vetable-dataset-without-duplicacy  

Fruit Freshness Dataset (Apple, Banana, Orange):  
  https://www.kaggle.com/datasets/user2036/fruit-freshness-dataset-v1  

- Includes both **fresh and rotten samples**  
- Covers multiple fruits and vegetables  
- Combined to improve model diversity and robustness

## 👩‍💻 Authors

- **Aishika Mitra** (23052052)
- **Barninee Samanta** (23052564)
- **Ananya Patra** (23052061)
- **Krittik Panda** (23051994)
- **Soumik Maiti** (23051790)
- **Souvik Mandal** (23052036)
**Project Guide:** Dr. Suchismita Das, School of Computer Engineering, KIIT University.
