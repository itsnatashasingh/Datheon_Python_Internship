# Task 1: Multi-Class Iris Classification Pipeline

## Project Overview

This project implements a multi-class classification pipeline using the Iris dataset as part of the Datheon Machine Learning & Data Science Internship.

The objective is to classify Iris flowers into three species:

- Setosa
- Versicolor
- Virginica

Two machine learning algorithms, Logistic Regression and Decision Tree Classifier, are implemented and evaluated.

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
Task_1_Iris_Classification/
│
├── Dataset/
│   └── iris.csv
│
├── notebook/
│   └── iris_classification.ipynb
│
└── README.md
```

## Implementation Workflow

### 1. Dataset Loading and Exploration
- Loaded the Iris dataset using Pandas.
- Examined dataset dimensions, data types, and statistical summaries.
- Checked for missing values.

### 2. Exploratory Data Analysis
- Visualized species distribution.
- Examined feature distributions using histograms.
- Analyzed pairwise feature relationships using pairplots.
- Generated a correlation heatmap.

### 3. Data Preprocessing
- Separated independent features and target labels.
- Encoded species labels using LabelEncoder.
- Split the dataset into training and testing sets using an 80:20 ratio.
- Standardized numerical features using StandardScaler.

### 4. Model Training
Implemented and trained:
- Logistic Regression
- Decision Tree Classifier

### 5. Model Evaluation
Evaluated both models using:
- Accuracy
- Precision
- Recall
- F1-score
- Classification reports

### 6. Model Visualization
- Generated confusion matrix heatmaps for both classifiers.
- Visualized decision boundaries using petal length and petal width.

## Model Performance

Both models achieved the following results on the testing dataset:

| Evaluation Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Accuracy | 93.33% | 93.33% |
| Precision | 93.33% | 93.33% |
| Recall | 93.33% | 93.33% |
| F1-score | 93.33% | 93.33% |

Both models correctly classified 28 out of 30 testing observations.

## Key Findings

- The dataset contains three equally represented Iris species.
- Petal length and petal width are useful features for distinguishing between species.
- Both models classified all Setosa testing observations correctly.
- The two models produced identical evaluation metrics and confusion matrices.
- Logistic Regression generated linear decision boundaries, while Decision Tree generated step-like decision regions.

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries:

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Open the project folder in VS Code.
4. Open the Jupyter Notebook:

`notebook/iris_classification.ipynb`

5. Select a Python kernel and execute the notebook cells from top to bottom.

## Conclusion

The project successfully demonstrates a multi-class classification workflow using the Iris dataset. Both Logistic Regression and Decision Tree achieved an accuracy of 93.33%, providing an opportunity to compare two different classification approaches.

The implementation covers data exploration, preprocessing, model training, evaluation, and visualization.