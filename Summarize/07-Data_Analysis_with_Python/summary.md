# Data Analysis with Python

## Key Concepts

### 1. Introduction to Data Analysis
- **Data Analysis**: The process of inspecting, cleansing, transforming, and modeling data to discover useful information, draw conclusions, and support decision-making.
- **Data Analysis Workflow**: Data Collection → Data Preparation → Data Exploration → Analysis → Interpretation → Communication
- **Types of Analysis**: Descriptive, Diagnostic, Predictive, Prescriptive

### 2. NumPy (Numerical Python)
- **Core Library**: Foundation for scientific computing in Python
- **Key Features**: 
  - Multi-dimensional array objects
  - Fast mathematical operations on arrays
  - Broadcasting functionality
  - Memory-efficient operations
- **Applications**: Used in linear algebra, random number generation, Fourier transforms

### 3. Descriptive Statistics
- **Measures of Central Tendency**: Mean, Median, Mode
- **Measures of Dispersion**: Range, Variance, Standard Deviation, IQR
- **Quantiles and Percentiles**: Quartiles (25%, 50%, 75%)
- **Distribution Shapes**: Symmetric, Skewed, Kurtosis

### 4. Pandas
- **Data Structures**: DataFrame and Series
- **Data Manipulation**: Reading, filtering, sorting, grouping, joining data
- **Data Cleaning**: Handling missing values, duplicates, outliers
- **Data Analysis**: Statistical functions, time series analysis

### 5. Exploratory Data Analysis (EDA)
- **Purpose**: Understand data patterns, spot anomalies, test hypotheses, check assumptions
- **Techniques**:
  - Univariate Analysis: Understanding single variables
  - Bivariate Analysis: Relationships between two variables
  - Multivariate Analysis: Relationships between multiple variables
- **Visualization Tools**: Matplotlib, Seaborn, Plotly

## Logical Flow of Ideas

1. **Foundation Setup**
   - Understanding the data analysis process
   - Setting up the environment with necessary libraries

2. **Data Acquisition and Understanding**
   - Loading data from various sources
   - Understanding data structure and features

3. **Data Preparation**
   - Data cleaning (handling missing values, outliers)
   - Feature engineering
   - Data transformation

4. **Exploratory Analysis**
   - Statistical summaries
   - Visualizations
   - Pattern discovery

5. **Analysis and Interpretation**
   - Drawing insights from data
   - Making data-driven decisions

## Important Syntax

### NumPy
```python
import numpy as np

# Creating arrays
arr = np.array([1, 2, 3, 4, 5])
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Array operations
np.mean(arr)       # Mean
np.median(arr)     # Median
np.std(arr)        # Standard deviation
np.var(arr)        # Variance

# Array manipulation
np.reshape(arr, (5, 1))     # Reshape
np.concatenate((arr1, arr2)) # Concatenate
```

### Pandas
```python
import pandas as pd

# Reading data
df = pd.read_csv('filename.csv')
df = pd.read_excel('filename.xlsx')
df = pd.read_sql(query, connection)

# Basic operations
df.head()          # First 5 rows
df.tail()          # Last 5 rows
df.info()          # DataFrame information
df.describe()      # Statistical summary
df.shape           # Dimensions of DataFrame

# Data manipulation
df['column_name']                # Select column
df[df['column'] > value]         # Filter rows
df.groupby('column').mean()      # Group by operations
df.sort_values('column')         # Sort values
df.pivot_table(index='A', columns='B', values='C') # Pivot tables

# Handling missing values
df.isna().sum()                  # Count missing values
df.dropna()                      # Drop missing values
df.fillna(value)                 # Fill missing values
```

### Data Visualization
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Matplotlib basic plots
plt.figure(figsize=(10, 6))
plt.plot(x, y)
plt.scatter(x, y)
plt.hist(data)
plt.bar(x, height)
plt.boxplot(data)
plt.title('Title')
plt.xlabel('X Label')
plt.ylabel('Y Label')
plt.show()

# Seaborn plots
sns.set_theme()                  # Set theme
sns.histplot(data=df, x='column', kde=True)
sns.boxplot(data=df, x='column')
sns.countplot(data=df, x='column')
sns.heatmap(corr_matrix, annot=True)
sns.pairplot(df)
```

## Key Definitions

1. **Array**: A collection of elements, usually of the same type, stored in contiguous memory.

2. **DataFrame**: A two-dimensional, size-mutable, potentially heterogeneous tabular data structure with labeled axes.

3. **Series**: A one-dimensional labeled array capable of holding data of any type.

4. **Data Cleaning**: The process of detecting and correcting (or removing) corrupt or inaccurate records from a dataset.

5. **Exploratory Data Analysis (EDA)**: An approach to analyzing data sets to summarize their main characteristics, often with visual methods.

6. **Feature Engineering**: The process of transforming raw data into features that better represent the underlying problem.

7. **Missing Values**: Data points that have no value in the dataset.

8. **Outliers**: Data points that differ significantly from other observations.

9. **Correlation**: A statistical measure that expresses the extent to which two variables are linearly related.

10. **Statistical Distribution**: The collection of all possible values of a random variable, along with their corresponding probabilities.

11. **Data Profiling**: The process of examining the data available in a data source and collecting statistics and information about that data.

12. **Univariate Analysis**: Analysis conducted on a single variable, primarily to describe the data and find patterns.

13. **Bivariate Analysis**: Analysis conducted to find the relationship between two variables.

14. **Multivariate Analysis**: Analysis conducted to find patterns in high-dimensional data.

15. **Data Visualization**: The graphical representation of data and information using visual elements like charts, graphs, and maps.