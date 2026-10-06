
# KNN Customer Purchase Prediction

## Project Overview

This project applies the **K-Nearest Neighbors (KNN)** classification algorithm to predict whether a customer will purchase a product based on their **age** and **estimated salary**.

The project demonstrates a complete basic classification workflow, including data preparation, train-test splitting, feature scaling, model training, evaluation, and comparison of different values of K.

## Dataset

The dataset contains **400 observations** and three variables:

| Feature | Description |
|---|---|
| Age | Customer's age |
| EstimatedSalary | Customer's estimated annual salary |
| Purchased | Purchase outcome (0 = No, 1 = Yes) |

The dataset contains no missing values in these variables.

## Machine Learning Workflow

The project includes:

- Data inspection and preprocessing
- Feature and target selection
- Train-test split
- Feature standardization using `StandardScaler`
- KNN classification
- Evaluation of K values from 1 to 29
- Accuracy comparison and visualization
- Model performance evaluation

## Feature Scaling

Because KNN is a distance-based algorithm, feature scaling was applied after splitting the data.

`StandardScaler` was fitted only on the training set and then used to transform both the training and test sets. This avoids data leakage from the test set.

## K Selection

Different values of K from **1 to 29** were evaluated.

The highest observed test accuracy was:

**93.75%**

Several K values achieved this accuracy, with **K = 7** being the first.

The accuracy-versus-K analysis also showed that performance remained relatively stable across several larger K values.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook / Google Colab

## Key Learning Points

This project demonstrates several important concepts in classification:

- Why feature scaling is particularly important for distance-based algorithms such as KNN
- Why preprocessing should be fitted only on training data
- How the number of neighbors affects KNN predictions
- How model performance can be compared across different hyperparameter values
- Why test data should remain independent from the model-training process

## Future Improvement

A stronger model-selection approach would use cross-validation on the training set to select K, followed by a single evaluation on the held-out test set. Additional metrics such as precision, recall, F1-score, and the confusion matrix can also provide a more complete assessment of classification performance.
