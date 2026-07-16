# Neurofive ML Track

This repository documents my progress through the **Neurofive Machine Learning Track**, where I complete hands-on tasks to build practical machine learning and data analysis skills.

## Repository Structure

```
neurofive-ml-track/
│── Titanic_EDA.ipynb
└── README.md
```

---

## Dataset

**Titanic – Machine Learning from Disaster**

The dataset contains passenger information such as age, gender, ticket class, fare, and survival status. It is widely used for learning data analysis, visualization, and machine learning fundamentals.
### Results

- **Algorithm:** Logistic Regression
- **Training/Test Split:** 80% / 20%
- **Accuracy:** **78.21%**

#### Confusion Matrix

| Actual \ Predicted | Did Not Survive | Survived |
|--------------------|----------------:|----------:|
| Did Not Survive | 89 | 16 |
| Survived | 23 | 51 |

### Conclusion

The Logistic Regression model achieved an accuracy of **78.21%** on the Titanic dataset. The model successfully classified most passengers, correctly predicting 140 out of 179 test samples. The confusion matrix revealed both correct predictions and misclassifications, demonstrating the importance of evaluating a model using multiple metrics rather than relying solely on accuracy.

---

## Task 1: Exploratory Data Analysis (EDA)

### Objectives
- Set up a Python environment using Google Colab
- Load the Titanic dataset with Pandas
- Explore the dataset using:
  - `head()`
  - `info()`
  - `describe()`
- Identify:
  - Dataset dimensions
  - Missing values
  - Numerical and categorical columns
- Summarize findings through a short data story

### Key Findings
- Dataset contains **891 rows** and **12 columns**.
- Missing values were found in the **Age**, **Cabin**, and **Embarked** columns.
- The dataset includes both numerical and categorical features, requiring preprocessing before machine learning.

---

## Task 2: Data Cleaning & Visualization

### Objectives
- Handle missing values using appropriate techniques
- Detect outliers using boxplots
- Visualize the dataset using Matplotlib and Seaborn
- Interpret visualizations to understand factors affecting survival

### Data Cleaning
- Filled missing values in **Age** using the median.
- Filled missing values in **Embarked** using the mode.
- Removed the **Cabin** column due to a large number of missing values.

### Visualizations Created
- Histogram of passenger ages
- Boxplot of passenger fares for outlier detection
- Bar chart showing survival counts
- Correlation heatmap of numerical features
- *(Optional)* Survival by gender visualization

### Key Insight
The analysis suggests that **Sex** has the strongest relationship with survival, as female passengers had a significantly higher survival rate than male passengers. Passenger class also appears to influence survival, with first-class passengers generally experiencing better outcomes.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Notebook

All tasks are completed in a single notebook:

- **Titanic_EDA.ipynb**

---

## Learning Outcomes

Through these tasks, I learned how to:

- Perform Exploratory Data Analysis (EDA)
- Identify and handle missing data
- Detect outliers using boxplots
- Create meaningful visualizations
- Extract insights from real-world datasets
- Prepare data for future machine learning models

---

## Author

**Abeerah Ateeq**

This repository will be updated as I continue progressing through the Neurofive Machine Learning Track.
