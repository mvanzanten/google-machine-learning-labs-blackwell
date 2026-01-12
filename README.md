# Google Machine Learning Labs (TensorFlow NGC (Blackwell Optimized))

This repository contains hands-on machine learning exercises from the [Google Machine Learning Crash Course](https://developers.google.com/machine-learning). These interactive Jupyter notebooks provide practical experience with fundamental ML concepts. The container utilized and the configuration is designed to operate with NVIDIA Blackwell GPUs (RTX 50xx).

## Contents

### 1. Linear Regression - Taxi Fare Prediction
**File:** `linear_regression_taxi.ipynb`

Learn how to build a linear regression model to predict taxi fares in Chicago. This notebook covers:
- Loading and exploring datasets using pandas
- Data visualization with Python libraries
- Feature engineering and selection
- Building and tuning a linear regression model
- Evaluating model performance using RMSE and loss curves

**Dataset:** Chicago Taxi Trips dataset (2-day subset from May 2022)

**Learning Objectives:**
- Read CSV files into pandas DataFrames
- Explore datasets with visualization
- Experiment with different features
- Tune model hyperparameters
- Compare training runs using metrics

### 2. Binary Classification - Rice Species Classification
**File:** `binary_classification_rice.ipynb`

Build a binary classifier to distinguish between two species of Turkish rice. This notebook teaches:
- Binary classification fundamentals
- Training a binary classifier
- Calculating and interpreting classification metrics
- Comparing AUC and ROC curves
- Threshold optimization

**Dataset:** Cinar and Koklu 2019 Osmancik and Cammeo Rice Dataset
- Measurements derived from rice grain images
- Two rice species classification task
- CC0 license

**Learning Objectives:**
- Train binary classifiers
- Calculate metrics at different thresholds
- Compare model performance using AUC and ROC

## References

- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning)
- [Jupyter Notebook Documentation](https://jupyter.org/)
- Rice Dataset Citation: Cinar, I. and Koklu, M., (2019). "Classification of Rice Varieties Using Artificial Intelligence Methods." *International Journal of Intelligent Systems and Applications in Engineering*, 7(3), 188-194.

## License
These exercises are part of Google's ML Crash Course educational materials.
