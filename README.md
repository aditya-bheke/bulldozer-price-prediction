# Bulldozer Price Prediction

## Overview

This project builds a machine learning regression model to predict the auction sale price of bulldozers using historical sales data.

The problem is based on the Kaggle competition **Bluebook for Bulldozers**. The objective is to estimate `SalePrice` using machine characteristics, usage information, and time-based features derived from the sale date.

---

## Problem Statement

Given historical auction data for bulldozers, predict the future sale price of machines in a test dataset.

This is a supervised regression problem evaluated using **Root Mean Squared Log Error (RMSLE)**.

---

## Dataset

Source: Kaggle – Bluebook for Bulldozers Competition

The dataset includes:

- Training dataset (with SalePrice)
- Validation dataset
- Test dataset (without SalePrice)
- Data dictionary describing feature definitions

The dataset is not included in this repository due to GitHub file size limits.

### To Use the Dataset

1. Download the dataset from Kaggle.
2. Create a folder named `data/` in the project root directory.
3. Place all dataset files inside the `data/` folder.

Expected structure:

```
bulldozer-price-prediction/
│
├── data/
│   ├── TrainAndValid.csv
│   ├── Test.csv
│   ├── Valid.csv
│   └── Data Dictionary.xlsx
```

---

## Project Structure

```
bulldozer-price-prediction/
│
├── notebooks/
│   └── end-to-end-bulldozer-price-regression.ipynb
│
├── README.md
├── environment.yml
└── .gitignore
```

- `notebooks/` contains the full end-to-end machine learning workflow.
- `environment.yml` defines required dependencies.
- `.gitignore` prevents large datasets and temporary files from being tracked.

---

## Approach

### 1. Data Exploration
- Inspect dataset structure
- Analyze missing values
- Understand feature distributions

### 2. Data Preprocessing
- Convert sale date into datetime format
- Extract time-based features (year, month, day)
- Handle missing values
- Encode categorical variables

### 3. Feature Engineering
- Transform categorical variables into numeric representations
- Create structured time-based features
- Ensure consistent feature alignment for test data

### 4. Model Training
- Random Forest Regressor
- Time-based validation split

### 5. Evaluation
- Metric: Root Mean Squared Log Error (RMSLE)
- Validation based on temporal split (not random split)

---

## Evaluation Metric

**RMSLE (Root Mean Squared Log Error)**

RMSLE is used because:
- It penalizes large errors more heavily
- It works well for skewed price distributions
- It evaluates relative differences rather than absolute differences

---

## Results

- Model: Random Forest Regressor
- Evaluation Metric: RMSLE
- Validation Score: <insert your final RMSLE score here>

---

## How to Run

### 1. Clone Repository

```
git clone https://github.com/aditya-bheke/bulldozer-price-prediction.git
cd bulldozer-price-prediction
```

### 2. Create Environment

Using Conda:

```
conda env create -f environment.yml
conda activate <environment-name>
```

Or using pip:

```
pip install -r requirements.txt
```

### 3. Download Dataset

Download dataset from Kaggle and place it inside the `data/` folder.

### 4. Run Notebook

Open and execute:

```
notebooks/end-to-end-bulldozer-price-regression.ipynb
```

Run all cells sequentially.

---

## Skills Demonstrated

- Data cleaning and preprocessing for tabular datasets
- Feature engineering with time-series components
- Handling categorical variables
- Model training and validation strategy design
- Regression model evaluation using RMSLE
- Clean machine learning project structuring

---

## License

This project is created for educational and portfolio purposes.
