# Spaceship Titanic Kaggle Competition

## Overview
This repository contains my solution for the Kaggle competition [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic). The goal of the competition is to predict whether passengers will be transported to another dimension based on various features.

## Contents
- `src/`
  - `analysis.ipynb`: Exploratory data analysis and insights from the dataset.
  - `main_ohe.ipynb`: Main notebook implementing the model using One-Hot Encoding for categorical features.
  - `main_loo.ipynb`: Main notebook implementing the model using Leave-One-Out Encoding for categorical features.

## Getting Started
To run the notebooks in this repository, make sure you have the required libraries installed. You can install them using pip:

```bash
pip install pandas numpy torch torchmetrics scikit-learn category-encoders
```

## Notebooks Description
### `analysis.ipynb`
This notebook conducts a thorough exploratory data analysis (EDA) on the Spaceship Titanic dataset. It provides insights into the data distribution, relationships between features, and potential strategies for feature engineering.

### `main_ohe.ipynb`
This notebook implements the neural network model using One-Hot Encoding (OHE) to handle categorical features. The encoding creates binary columns for each category, which can increase the dimensionality of the dataset but can effectively represent the information for certain models.

### `main_loo.ipynb`
This notebook implements the neural network model using Leave-One-Out Encoding (LOO). In this method, each category's encoding is the mean of the target variable (Transported) for that category, calculated from the training data. This approach is particularly useful for reducing dimensionality and preventing overfitting when dealing with categorical features, especially in cases where categories have varying frequencies.

## How to Run
Clone this repository to your local machine.
Navigate to the folder containing the notebooks.
Open the desired notebook in Jupyter Notebook or any compatible environment.
Run the cells sequentially to reproduce the analysis or model training.

## Results
The final predictions can be found in the output of each notebook after running the model. The predictions indicate whether each passenger was transported (True) or not (False).
Saving the model or the results is commented.

### Kaggle Results for Leave One Out encoding method:
**0.75099** image in (image_titanic_spaceshit_loo.png)

### Kaggle Results for One Hot encoding method:
**0.73158** image in (image_titanic_spaceshit_ohe.png)

## Conclusion
This project showcases the application of various encoding techniques in a neural network context for binary classification tasks. Each encoding method presents unique advantages and trade-offs that can impact model performance.

