# Tools for Data Science - Quiz

## Multiple Choice Questions

1. **Which of the following is NOT considered one of the main categories of data science tools?**
   - A) Programming Languages
   - B) Data Management Tools
   - C) Hardware Components
   - D) Visualization Tools

2. **Which programming language is specifically designed for statistical analysis and visualization?**
   - A) Python
   - B) R
   - C) SQL
   - D) Java

3. **Which of the following is a key feature of Jupyter Notebooks?**
   - A) Only supports R programming language
   - B) Requires local installation and cannot be used in the cloud
   - C) Supports combining markdown text with executable code
   - D) Limited to only text output with no visualization capabilities

4. **Which Python library is primarily used for data manipulation and analysis?**
   - A) Matplotlib
   - B) NumPy
   - C) pandas
   - D) TensorFlow

5. **In the data science workflow, when should you select visualization tools?**
   - A) Only at the beginning of the project
   - B) After data collection but before data cleaning
   - C) After data manipulation, during the exploratory phase
   - D) Only at the very end when presenting to stakeholders

6. **Which of these is NOT a commonly used SQL command in data science?**
   - A) SELECT
   - B) UPDATE
   - C) DEPLOY
   - D) JOIN

7. **What is Hadoop primarily used for?**
   - A) Creating interactive dashboards
   - B) Statistical analysis
   - C) Processing large datasets in a distributed manner
   - D) Front-end web development

## Short Answer Questions

8. **Explain the difference between a library and a framework in the context of data science tools.**

9. **Name three Python libraries used for data visualization and briefly describe what makes each one unique.**

10. **What is the purpose of ETL in data science projects? List the three stages it represents and briefly explain each one.**

11. **Compare and contrast Jupyter Notebooks and traditional IDEs (like VS Code) for data science work. When might you prefer one over the other?**

12. **Describe how version control tools like Git benefit data science projects and collaboration.**

## Practical Exercises

13. **Python Library Identification:**  
    For each of the following tasks, identify the most appropriate Python library/package:
    - a) Creating a pandas DataFrame from a CSV file
    - b) Computing the mean, median, and standard deviation of a dataset
    - c) Creating a heatmap to visualize correlation between variables
    - d) Building and training a random forest classifier
    - e) Processing and analyzing text data for sentiment analysis

14. **SQL Query Exercise:**  
    Write a simple SQL query that would:
    - Select customer names and their total purchases
    - From a table called 'customers' joined with 'orders'
    - Group results by customer
    - Show only customers who spent more than $1000

15. **Development Environment Selection:**  
    For each of the following scenarios, recommend the most appropriate development environment and explain why:
    - a) A data scientist needs to create a shareable document with code, visualizations, and narrative text to explain findings to non-technical stakeholders.
    - b) A team of data engineers is building a production-ready data pipeline that will run on a schedule.
    - c) A statistician familiar with R needs to conduct complex statistical analyses and create publication-quality graphics.
    - d) A beginner is learning data science and needs access to computing resources they don't have locally.

---

**Answers:**
1. C - Hardware Components are not typically classified as a main category of data science tools.
2. B - R is specifically designed for statistical analysis and visualization.
3. C - Jupyter Notebooks support combining markdown text with executable code.
4. C - pandas is primarily used for data manipulation and analysis.
5. C - Visualization tools are typically used after data manipulation, during the exploratory phase.
6. C - DEPLOY is not a standard SQL command; the others are common SQL operations.
7. C - Hadoop is used for processing large datasets in a distributed manner.
8. A library is a collection of pre-written code that users can reuse for specific functions (like pandas for data manipulation), while a framework provides a structure and foundation for developing applications, often dictating the flow of the application (like Django for web applications).
9. Matplotlib (low-level, highly customizable plotting library), Seaborn (statistical visualization based on matplotlib with a higher-level interface), Plotly (interactive visualizations for web applications), Bokeh (interactive visualization targeting web browsers).
10. ETL stands for Extract, Transform, Load. Extract involves gathering data from various sources. Transform involves cleaning, formatting, and making the data suitable for analysis. Load involves storing the processed data in a target system like a data warehouse or database for analysis.
11. Jupyter Notebooks excel at interactive exploration, combining code with narrative and direct visualization, making them ideal for experimentation and storytelling. Traditional IDEs like VS Code offer better support for large codebases, debugging tools, and integration with software development practices. Notebooks are preferred for exploration and presentation; IDEs for production code and larger projects.
12. Git enables tracking changes to code over time, allowing data scientists to experiment while maintaining the ability to revert to previous versions. It facilitates collaboration by allowing multiple team members to work on the same project simultaneously without conflicts. It also documents the evolution of analyses and models, providing reproducibility and transparency.
13. a) pandas, b) NumPy or pandas, c) Seaborn, d) Scikit-learn, e) NLTK or spaCy
14. ```sql
    SELECT c.customer_name, SUM(o.amount) as total_purchases
    FROM customers c
    INNER JOIN orders o ON c.customer_id = o.customer_id
    GROUP BY c.customer_name
    HAVING SUM(o.amount) > 1000;
    ```
15. a) Jupyter Notebook, because it combines code, visualizations, and narrative text in a shareable document format.
    b) VS Code or PyCharm, because they provide better support for production code, debugging, and integration with CI/CD pipelines.
    c) RStudio, because it's specifically designed for R programming with integrated statistical tools and visualization capabilities.
    d) Google Colab, because it provides free access to computing resources including GPUs and requires no local installation.