
# Classification Models - Titanic Dataset

## Overview
This project implements multiple classification models on the Titanic dataset to predict passenger survival. The best performing model is **Support Vector Machine (SVM)** with an accuracy score of **82%**.

## Data Cleaning & Preprocessing

### 1. Data Exploration
- Loaded the Titanic dataset using Seaborn
- Identified redundant and null-filled columns

### 2. Data Cleaning
Removed redundant columns:
- `who`, `adult_male` (duplicates of `sex`)
- `class` (duplicate of `pclass`)
- `alive` (duplicate of `survived`)
- `embark_town` (duplicate of `embarked`)
- `deck` (excessive missing values)

Handled missing values:
- Filled `age` column with mean value
- Dropped rows with missing `embarked` values

### 3. Feature Encoding
Applied **Label Encoding** to categorical variables:
- `sex` → numeric values
- `embarked` → numeric values
- `alone` → integer conversion

### 4. Feature Scaling
Applied **StandardScaler** to numerical features with large value ranges:
- `age` - scaled to normalize across passengers
- `fare` - scaled due to wide value range

## Model Development

Built and evaluated 5 classification models:

1. **Logistic Regression** - F1 Score: 84%
2. **K-Nearest Neighbors (KNN)**
3. **Naive Bayes**
4. **Decision Tree**
5. **Support Vector Machine (SVM)** - **Best Model: 82% Accuracy**

## Dataset Split
- Training set: 80%
- Test set: 20%
- Random state: 42

## Best Model
**Support Vector Machine (SVM)** with RBF kernel achieved the highest accuracy and is recommended for deployment.
