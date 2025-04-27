# Data Cleaning and Preprocessing Notebook

## Overview
This Jupyter notebook demonstrates a comprehensive data cleaning and preprocessing workflow using the Titanic dataset. The notebook covers:

- Data import and initial exploration
- Handling missing values
- Label encoding for categorical variables
- Feature scaling/normalization
- Outlier detection and visualization

## Key Steps

### 1. Data Import and Exploration
- Loads the Titanic dataset from a CSV file.
- Uses `df.info()` to examine data structure and types.
- Checks for missing values with `df.isnull().sum()`.
- Displays the first few rows with `df.head()`.

### 2. Handling Missing Values
- **Numeric columns**: Fills missing values with the **median**.
- **Categorical columns**: Fills missing values with the **mode** (most frequent value).
- Choice Explanation:
  - Median is robust to outliers.
  - Mode is appropriate for categorical data.

### 3. Label Encoding
- Uses scikit-learn's `LabelEncoder` to convert categorical variables to numeric.
- Transforms all `object` type columns for machine learning compatibility.

### 4. Feature Scaling
- Applies `StandardScaler` to normalize numerical features.
- **Why?** Standardization (mean=0, std=1) is important for many ML algorithms to perform optimally.

### 5. Outlier Visualization
- Creates boxplots for numerical features to identify potential outliers.
- Uses **Seaborn** for visualization.

---

## Questions and Answers

### 1. What is the purpose of EDA?
Exploratory Data Analysis (EDA) helps understand the main characteristics of a dataset, discover patterns, spot anomalies, test hypotheses, and check assumptions before applying more advanced analysis or machine learning techniques.

### 2. How do boxplots help in understanding a dataset?
Boxplots visually show the distribution of data through quartiles, highlighting:
- The median (central line)
- Interquartile range (IQR - the box)
- Potential outliers (points outside whiskers)
- Data spread and skewness

### 3. What is correlation and why is it useful?
Correlation measures the statistical relationship between two variables (-1 to 1). It's useful for:
- Identifying relationships between features
- Detecting multicollinearity
- Feature selection
- Understanding data patterns

### 4. How do you detect skewness in data?
Skewness can be detected by:
- Visual inspection (histograms, density plots)
- Calculating skewness coefficient (positive/negative/zero)
- Comparing mean and median (differences suggest skewness)
- Using Q-Q plots

### 5. What is multicollinearity?
Multicollinearity occurs when independent variables in a regression model are highly correlated. This can:
- Make coefficient estimates unstable
- Reduce model interpretability
- Inflate variance of coefficient estimates

### 6. What tools do you use for EDA?
Common EDA tools include:
- **Python libraries**: Pandas, NumPy, Matplotlib, Seaborn, Plotly
- **Statistical tools**: SciPy, Statsmodels
- **Visualization**: Tableau, Power BI
- **Notebook environments**: Jupyter, Google Colab

### 7. Can you explain a time when EDA helped you find a problem?
In this Titanic dataset, EDA revealed:
- Missing values in **Age** (177), **Cabin** (687), and **Embarked** (2) columns.
- Potential outliers in numerical features through boxplots.
- The need for encoding categorical variables like **Sex** and **Embarked**.
- The importance of feature scaling due to different feature ranges.

### 8. What is the role of visualization in ML?
Visualization helps with:
- Understanding data distributions
- Identifying patterns and relationships
- Detecting outliers and anomalies
- Feature selection and engineering
- Model evaluation and interpretation
- Communicating results to stakeholders

---

## Usage

To run this notebook:

1. Ensure you have **Python** and **Jupyter Notebook** installed.
2. Install required packages:
    ```bash
    pip install pandas numpy scikit-learn seaborn
    ```
3. Update the file path to point to your **Titanic** dataset.
4. Run the cells sequentially.

---

