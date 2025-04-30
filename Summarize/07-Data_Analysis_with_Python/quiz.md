# Data Analysis with Python - Quiz

## Multiple Choice Questions

### NumPy Basics
1. Which NumPy function would you use to compute the mean of elements in an array?
   - A. np.average()
   - B. np.mean()
   - C. np.median()
   - D. np.sum() / len(array)

2. What does the following code snippet do?
   ```python
   arr = np.arange(10).reshape(2, 5)
   ```
   - A. Creates a 1D array with 10 elements
   - B. Creates a 2D array with shape (2, 5)
   - C. Creates a 5D array with shape (2)
   - D. Raises an error

### Pandas Fundamentals

3. Which method is used to display the first 5 rows of a DataFrame?
   - A. df.top()
   - B. df.first()
   - C. df.head()
   - D. df.preview()

4. Which statement correctly filters a DataFrame `df` to show rows where the column 'age' is greater than 30?
   - A. df.where('age' > 30)
   - B. df.query('age > 30')
   - C. df[df.age > 30]
   - D. df.filter('age > 30')

5. What does `df.describe()` provide?
   - A. A description of the DataFrame structure
   - B. Statistical summary of numerical columns
   - C. A list of all columns and their data types
   - D. The source of the data in the DataFrame

### Data Cleaning

6. What's the recommended approach for handling missing values in a column that has ~5% missing data?
   - A. Drop the entire column
   - B. Drop rows with missing values
   - C. Fill missing values with mean/median
   - D. Leave them as missing

7. The IQR method is commonly used for:
   - A. Handling missing values
   - B. Feature scaling
   - C. Detecting outliers
   - D. Data normalization

### Exploratory Data Analysis

8. Which type of plot would be most appropriate for visualizing the relationship between two numerical variables?
   - A. Bar plot
   - B. Histogram
   - C. Scatter plot
   - D. Pie chart

9. What does univariate analysis focus on?
   - A. The relationship between two variables
   - B. The distribution of a single variable
   - C. The interaction between multiple variables
   - D. Statistical hypothesis testing

10. Which plotting library is built on top of Matplotlib and provides a higher-level interface for visualization?
    - A. Plotly
    - B. Seaborn
    - C. Bokeh
    - D. ggplot

## Practical Exercises

### Exercise 1: NumPy Array Manipulation
Write a function that takes a 1D NumPy array as input and returns a new array with the following characteristics:
- All elements are squared
- Elements greater than 25 are replaced with 25
- The mean of the resulting array is calculated and returned as well

### Exercise 2: Pandas Data Cleaning
Given a DataFrame with columns 'age', 'income', and 'education', perform the following operations:
1. Check for missing values
2. Fill missing 'age' values with the median age
3. Fill missing 'income' values with the mean grouped by 'education'
4. Remove any remaining rows with missing values
5. Identify outliers in 'income' using the IQR method

### Exercise 3: Data Visualization
Create a visualization script that takes a dataset and produces:
1. A histogram for a numerical column
2. A boxplot comparing the numerical column across different categories
3. A correlation heatmap if multiple numerical columns exist
4. A pairplot for numerical columns, colored by a categorical variable

### Exercise 4: Exploratory Data Analysis
Using a dataset of your choice (e.g., the Titanic dataset):
1. Perform univariate analysis on numerical and categorical features
2. Conduct bivariate analysis to find relationships between features
3. Create a pivot table to understand the interaction between two categorical variables and their effect on a numerical variable
4. Draw conclusions about key factors that influence the target variable

## Answers
The answers are provided at the end of this document for self-assessment.

1. B
2. B
3. C
4. C
5. B
6. B
7. C
8. C
9. B
10. B