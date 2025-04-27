# Data Preprocessing for Machine Learning

This repository contains code for preprocessing datasets for machine learning applications. The code implements several essential data preparation steps to ensure your data is ready for modeling.

## Steps Included

### 1. Handling Missing Values
The code provides methods to handle missing values in both numerical and categorical columns:
- **Numerical columns** - Filled using the median value
- **Categorical columns** - Filled using the mode (most frequent value)

### 2. Converting Categorical Features to Numerical
Implements Label Encoding to convert categorical variables into numerical format.

### 3. Standardizing Numerical Features
Uses StandardScaler to transform numerical features to have mean=0 and standard deviation=1.

### 4. Outlier Detection and Removal
Visualizes outliers using boxplots and removes them using the IQR method.

## FAQ

### What is the purpose of EDA?
Exploratory Data Analysis helps understand dataset characteristics, identify patterns, anomalies, and relationships before modeling. It informs preprocessing decisions and provides insights into the data structure.

### How do boxplots help in understanding a dataset?
Boxplots provide visual summaries of numerical distributions, showing median values, interquartile ranges, and potential outliers. They help assess symmetry/skewness and quickly identify unusual values.

### What is correlation and why is it useful?
Correlation measures relationships between variables, which helps with feature selection, detecting multicollinearity, and understanding variable interactions before modeling.

### How do you detect skewness in data?
Skewness can be detected through visual methods (histograms, boxplots), statistical tests (skewness coefficients), and QQ plots comparing distributions to normal distributions.

### What is multicollinearity?
Multicollinearity occurs when independent variables are highly correlated, making model coefficients unstable and difficult to interpret. It's typically detected using correlation matrices or VIF analysis.

### What tools do you use for EDA?
Common EDA tools include Pandas for data manipulation, Matplotlib/Seaborn for visualization, Scikit-learn for preprocessing, and various statistical methods.

### What is the role of visualization in ML?
Visualization helps with data understanding, guides feature engineering decisions, communicates findings to stakeholders, and assists in model evaluation.

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Installation
```
pip install pandas numpy scikit-learn matplotlib seaborn
```