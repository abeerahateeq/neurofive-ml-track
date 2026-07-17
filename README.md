# Neurofive ML Track

This repository documents my progress through the **Neurofive Machine Learning Track**, where I complete hands-on projects to build practical skills in data analysis, visualization, and machine learning using Python and scikit-learn.

---

## Repository Structure

```text
neurofive-ml-track/
│── Titanic_EDA.ipynb
│── California_Housing_Regression.ipynb
└── README.md
```

### Notebooks

#### 📊 Titanic_EDA.ipynb
Contains:
- **Task 1:** Exploratory Data Analysis (EDA)
- **Task 2:** Data Cleaning & Data Visualization
- **Task 3:** Logistic Regression Classification

#### 🏡 California_Housing_Regression.ipynb
Contains:
- **Task 4:** Linear Regression
- California Housing dataset
- Model evaluation using RMSE and R² Score
- Actual vs. Predicted Price visualization

---

# Task 1: Exploratory Data Analysis (EDA)

## Objectives

- Set up a Python environment using Google Colab
- Load the Titanic dataset using Pandas
- Explore the dataset using:
  - `head()`
  - `info()`
  - `describe()`
- Identify:
  - Dataset dimensions
  - Missing values
  - Numerical and categorical columns
- Summarize findings with a short data story

## Key Findings

- Dataset contains **891 rows** and **12 columns**.
- Missing values were found in the **Age**, **Cabin**, and **Embarked** columns.
- The dataset contains both numerical and categorical variables that require preprocessing before model training.

---

# Task 2: Data Cleaning & Visualization

## Objectives

- Handle missing values appropriately
- Detect outliers using boxplots
- Create meaningful visualizations
- Interpret data before building a machine learning model

## Data Cleaning

- Filled missing values in **Age** using the median.
- Filled missing values in **Embarked** using the mode.
- Removed the **Cabin** column because it contained a large number of missing values.

## Visualizations Created

- Histogram
- Boxplot
- Bar Chart
- Correlation Heatmap
- Survival by Gender (additional visualization)

## Key Insight

The analysis showed that **Sex** has the strongest relationship with survival. Female passengers had a considerably higher survival rate than male passengers. Passenger class also appeared to influence survival.

---

# Task 3: Logistic Regression Classification

## Objectives

- Encode categorical variables using One-Hot Encoding
- Split the dataset into training and testing sets
- Train a Logistic Regression classifier
- Evaluate the model using Accuracy Score
- Analyze performance using a Confusion Matrix

## Machine Learning Workflow

1. Cleaned the dataset.
2. Encoded categorical features (`Sex` and `Embarked`).
3. Split the data using `train_test_split`.
4. Trained a Logistic Regression model.
5. Evaluated performance using Accuracy Score and Confusion Matrix.

## Results

| Metric | Value |
|---------|------:|
| Accuracy | **78.21%** |

### Confusion Matrix

| Actual \ Predicted | Did Not Survive | Survived |
|--------------------|----------------:|----------:|
| Did Not Survive | 89 | 16 |
| Survived | 23 | 51 |

## Conclusion

The Logistic Regression model correctly classified **140 out of 179** passengers in the test dataset, achieving an accuracy of **78.21%**. The confusion matrix highlighted both successful predictions and classification errors, demonstrating the importance of evaluating a model beyond accuracy alone.

---

# Task 4: Linear Regression

## Objectives

- Load the California Housing dataset
- Select important features affecting house prices
- Train a Linear Regression model
- Evaluate the model using RMSE and R² Score
- Visualize predicted versus actual house prices

## Features Used

- Median Income
- House Age
- Average Rooms
- Average Bedrooms
- Population

## Results

| Metric | Value |
|---------|------:|
| RMSE | **0.802** |
| R² Score | **0.509** |

## Conclusion

The Linear Regression model explained approximately **50.9%** of the variation in house prices using the selected features. The RMSE of **0.802** indicates the average prediction error, while the R² score demonstrates that the selected features capture a substantial portion of the pricing patterns. Additional features and more advanced regression algorithms could further improve model performance.

---

# Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Data Visualization
- Logistic Regression
- Linear Regression
- Model Evaluation
- Classification
- Regression
- Machine Learning Fundamentals

---
# Task 5: Model Evaluation & Hyperparameter Tuning

## Objectives

- Evaluate the classification model beyond accuracy.
- Calculate Precision, Recall, and F1-score.
- Tune Logistic Regression using GridSearchCV.
- Compare the original and tuned models.

## Hyperparameters Tuned

- C (Regularization Strength)
- Solver

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score

## Results

| Model | Accuracy |
|--------|---------:|
| Original Logistic Regression | 78.21% |
| Tuned Logistic Regression | 78.21% |

## Conclusion

Hyperparameter tuning systematically searched for better model settings using cross-validation. Comparing the original and tuned models helped demonstrate whether adjusting the model's parameters improved its predictive performance.
# Task 6: Customer Churn Prediction

## Dataset

Telco Customer Churn (Kaggle)

## Objectives

- Perform Exploratory Data Analysis
- Train Logistic Regression
- Train Decision Tree
- Compare both models
- Identify important churn features
- Provide business recommendations

## Algorithms

- Logistic Regression
- Decision Tree Classifier

## Evaluation

- Accuracy Comparison
- Feature Importance

## Business Insight

Contract type, tenure, and monthly charges were identified as major factors influencing customer churn. These findings can support customer retention strategies and improve business decision-making.
# Task 7: Machine Learning Pipeline

## Objectives

- Build a preprocessing pipeline using ColumnTransformer
- Scale numerical features
- Encode categorical features
- Combine preprocessing and Logistic Regression into one Pipeline
- Engineer new features
- Save the trained pipeline using Joblib

## Feature Engineering

New features created:

- FamilySize
- IsAlone

## Technologies

- Pipeline
- ColumnTransformer
- StandardScaler
- OneHotEncoder
- Joblib

## Outcome

The pipeline automated preprocessing and model training in a single reusable workflow. Feature engineering added additional information about passengers, and the trained pipeline was saved for future inference or deployment.
# Task 8: Ensemble Learning

## Objective

Compare ensemble learning models with previously trained classification models using the Telco Customer Churn dataset.

## Models Compared

| Model | Accuracy |
|--------|---------:|
| Logistic Regression | **82.19%** |
| XGBoost | **79.42%** |
| Random Forest | **78.92%** |
| Decision Tree | **70.97%** |

## Key Findings

- Logistic Regression achieved the highest accuracy in this experiment.
- XGBoost and Random Forest performed competitively but did not surpass Logistic Regression using their default settings.
- Decision Tree produced the lowest accuracy, demonstrating how a single tree can overfit compared to ensemble methods.
- Ensemble methods provide additional benefits such as robustness and feature importance analysis, but they often require hyperparameter tuning to reach their full potential.

## Conclusion

This task reinforced that model performance depends on both the dataset and model configuration. While ensemble methods are often among the strongest performers, a well-suited simpler model like Logistic Regression can outperform them when evaluated with default parameters.
# Task 9: Handling Imbalanced Data

## Dataset

Telco Customer Churn

## Technique Used

- SMOTE (Synthetic Minority Oversampling Technique)

## Performance Comparison

| Metric | Before SMOTE | After SMOTE |
|---------|-------------:|------------:|
| Precision | **0.685** | **0.586** |
| Recall | **0.601** | **0.684** |
| F1 Score | **0.640** | **0.631** |

## Key Findings

- SMOTE successfully improved recall from **0.601** to **0.684**.
- Precision decreased because the model predicted more customers as likely to churn, increasing false positives.
- The slight reduction in F1-score highlights the trade-off between precision and recall.
- In customer retention, improving recall can be beneficial because identifying more at-risk customers allows businesses to intervene before they leave.
# Author

**Abeerah Ateeq**

This repository is continuously updated as I progress through the Neurofive Machine Learning Track, documenting my learning journey and hands-on machine learning projects.
