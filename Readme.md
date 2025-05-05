# Warfarin Dosage Prediction Using Machine Learning

## Abstract

This project aims to predict the stable warfarin dose required for patients based on their clinical, demographic, and genetic features using machine learning algorithms. Warfarin dosing is crucial as improper dosing can lead to serious health complications like bleeding or thrombosis. Our model helps personalize warfarin therapy to improve patient outcomes and safety.

---

## Data Description

The dataset includes patient information such as age, weight, height, race, INR levels, and genetic variants (e.g., VKORC1, CYP2C9). It is derived from the International Warfarin Pharmacogenetics Consortium (IWPC) and publicly available from [PharmGKB](https://www.pharmgkb.org/downloads).

### Key Features:

| Feature                      | Description                                   |
|-----------------------------|-----------------------------------------------|
| **Height**                  | Patient height in centimeters (float)         |
| **Weight**                  | Patient weight in kilograms (float)           |
| **Age**                     | Categorical age ranges (string)               |
| **Race**                    | Ethnic background (categorical)               |
| **INR on Therapeutic Dose** | Blood clotting ability (float)                |
| **Amiodarone Use**          | Binary flag for Amiodarone usage (0/1)        |
| **Genotype Variants**       | VKORC1 and CYP2C9 variants                    |
| **Therapeutic Dose of Warfarin** | Target variable (float)               |

---

## Data Preprocessing

- **Missing values** handled via median imputation for numerical features, mode for categorical.
- **Categorical variables** encoded using one-hot encoding.
- **Scaling** applied to numerical features using StandardScaler.

---

## Machine Learning Models Used

- **Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **Support Vector Regressor (SVR)**
- **Neural Network (MLPRegressor)**

---

## Evaluation Metrics

- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

---

## Results

| Model                   | RMSE  | MAE   | R² Score |
|------------------------|-------|-------|----------|
| Linear Regression      | 9.82  | 7.25  | 0.42     |
| Random Forest          | 8.13  | 6.04  | 0.61     |
| XGBoost                | 7.89  | 5.92  | 0.63     |
| SVR                    | 9.11  | 6.84  | 0.47     |
| Neural Network (MLP)   | 8.75  | 6.55  | 0.53     |

XGBoost provided the best results, with the highest R² score and lowest RMSE and MAE.

---


