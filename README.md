# Urine Bacteria Classifier

An improved machine learning model for automated classification of bacteria in urine samples using computer vision and advanced feature extraction techniques.


## Key Improvements

### Model Architecture
- **Upgraded Algorithm**: Switched from Random Forest to **XGBoost**
- **Enhanced Feature Extraction**: Transitioned from grayscale GLCM (Gray-Level Co-occurrence Matrix) to colored feature vectors
- **Color Space Optimization**: Migrated from grayscale to **HSV color space**

### Data Handling
- **Class Imbalance Solution**: Implemented SMOTE (Synthetic Minority Oversampling Technique) to address significant class imbalance

## Dataset

The model was trained and evaluated on a dataset of **1,500 images** with the following class distribution:

| Class | Count | Percentage |
|---------|-------|----------|
| Class A | 135 | 9.0%       |
| Class B | 363 | 24.2%      |
| Class C | 500 | 33.3%      |
| Class D | 40  | 2.7%       |
| Class E | 462 | 30.8%      |

**Note**: The dataset exhibits significant class imbalance, which is addressed through SMOTE oversampling.

## Performance

### Overall Accuracy: 91%

### Detailed Classification Report

```
                precision    recall  f1-score   support
Class A (0)         0.91      0.95      0.93       110
Class B (1)         0.87      0.91      0.89       100
Class C (2)         0.96      0.96      0.96       104
Class D (3)         0.99      1.00      0.99        94
Class E (4)         0.84      0.75      0.79        92

accuracy                                0.92       500
macro avg           0.91      0.91      0.91       500
weighted avg        0.91      0.92      0.91       500
```

### Key Performance Highlights
- **Best Performing Class**: Class D with 99% precision and 100% recall
- **Most Challenging Class**: Class E with 84% precision and 75% recall
- **Balanced Performance**: Macro average F1-score of 0.91 across all classes

## Technical Stack

- **Machine Learning**: XGBoost
- **Image Processing**: OpenCV, scikit-image
- **Data Balancing**: SMOTE (imbalanced-learn)
- **Feature Extraction**: HSV color space analysis
- **Evaluation**: scikit-learn metrics
