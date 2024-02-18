# Cutsomer-liability-using-R

![image](https://github.com/Noahkandie/Cutsomer-liability-using-R/assets/83200580/81e3526c-3c05-42a7-bac0-d2483b017489)

## 1. Package Installation and Loading:

The script begins by checking if the 'mlba' package is available. If not, it installs the package from GitHub and loads it along with other necessary libraries (devtools, caTools, class, tidyverse, dplyr, ggplot2, caret, pROC, mlbench).

## 2. Data Loading and Exploration:

The UniversalBank dataset from the 'mlba' package is loaded and examined. Basic summary statistics such as head(), str(), summary(), and checking for missing values and unique values are performed.
## 3. Data Preprocessing:

The ID and ZIP code columns are dropped from the dataset as they are unlikely to be predictive of the outcome.
Categorical variables are converted to factors.
New customer characteristics are defined for predicting loan acceptance for a hypothetical customer.

## 4. Model Building:

The dataset is split into training and holdout sets.
The k-NN model is initially built with k=1 using the entire training dataset.
A prediction is made for the new customer using the k-NN model.
## 5. Model Evaluation and Tuning:

Cross-validation (5-fold) is performed to find the optimal value of k.
A grid search is conducted for different values of k (from 1 to 25).
The optimal k value is determined from the cross-validated results.
The k-NN model is then rebuilt using the optimal k value.
Finally, the model's performance is visualized with a plot showing the optimal k for the k-NN model.
