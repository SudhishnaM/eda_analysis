# eda_analysis
# Exploratory Data Analysis (EDA) of Train Schedule Data

## Overview
This project performs Exploratory Data Analysis (EDA) on a dataset containing train schedules. The goal is to understand the structure of the data, clean and preprocess it, extract meaningful insights, and visualize key trends.

## 1. Data Loading and Initial Exploration
The dataset was loaded and initially inspected to understand its structure, column types, and missing values. Key steps included:
- **Reading the dataset**: The dataset was read using a data manipulation library like Pandas.
- **Displaying basic information**: Methods such as `.info()` and `.head()` were used to get an overview of the dataset.
- **Checking missing values**: `.isnull().sum()` helped identify missing data that required handling.
- **Descriptive statistics**: `.describe()` provided an overview of numerical attributes such as seat availability and distance.

## 2. Data Cleaning and Preprocessing
Several preprocessing steps were performed to ensure data quality:
- **Handling Missing Values**: Missing data was identified and either imputed or removed using functions like `.dropna()` or `.fillna()`.
- **Duplicate Removal**: Duplicate records were detected using `.duplicated().sum()` and removed with `.drop_duplicates()`.
- **Data Type Conversion**: Columns related to time were converted into datetime format using `pd.to_datetime()` for easier analysis.
- **Anomalous Value Detection**: Outliers in numerical data were identified using visualization techniques like boxplots.

## 3. Exploratory Data Analysis (EDA)
EDA techniques were applied to extract insights, including:
1. **Descriptive Statistics**: Functions like `.value_counts()` and `.groupby()` were used to summarize categorical and numerical data.
2. **Train Route Analysis**: Aggregation functions helped identify the longest and shortest routes based on distance.
3. **Timings Analysis**: The dataset was analyzed to find peak train arrival and departure times using time-based grouping.
4. **Seat Availability Trends**: Filtering and grouping techniques were used to analyze seat availability across different train classes.
5. **Correlation Analysis**: The `.corr()` function was used to examine relationships between numerical attributes like distance and seat availability.

## 4. Data Visualization
Various visualizations were employed to better understand the dataset:
- **Histograms & Boxplots**: Used with `matplotlib` and `seaborn` to analyze seat availability and distance distributions.
- **Scatter Plots**: Created using `seaborn.scatterplot()` to examine relationships between train distance and seat availability.
- **Time Series Analysis**: Train schedules and peak hours were visualized using `sns.lineplot()` to detect traffic patterns.
- **Bar Charts & Pie Charts**: Most frequently visited stations and class-wise seat distributions were represented using `sns.barplot()` and `plt.pie()`.

## Key Insights and Summary
- **Train Scheduling Patterns**: Certain stations experience higher train traffic, while others have limited service.
- **Seat Availability Insights**: Higher-class seats (1A, 2A) are typically more expensive but show lower availability, whereas sleeper class (SL) has higher availability.
- **Peak Hours**: Some stations have congestion during specific hours, which may require better scheduling for efficiency.
- **Data Quality Issues**: Some arrival and departure times were found to be unrealistic (e.g., 00:00:00), which could indicate missing data or errors in reporting.

