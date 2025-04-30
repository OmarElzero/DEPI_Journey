# Data Science Methodology - Quiz

## Multiple Choice Questions

1. **Which of the following is NOT a phase in the CRISP-DM methodology?**
   - A) Business Understanding
   - B) Data Understanding
   - C) Analytic Approach
   - D) Data Preparation

2. **What is the primary purpose of the "Business Understanding" phase?**
   - A) To collect all available data
   - B) To clearly define the business problem and objectives
   - C) To select the appropriate modeling algorithms
   - D) To clean and transform the data

3. **During which phase would you handle missing values and outliers?**
   - A) Data Understanding
   - B) Data Collection
   - C) Data Preparation
   - D) Modeling

4. **Which of the following is a key activity in the "Evaluation" phase?**
   - A) Collecting data from various sources
   - B) Creating new features from existing data
   - C) Determining if the model solves the business problem
   - D) Implementing the model into production systems

5. **What is "model drift"?**
   - A) When a model moves from testing to production
   - B) When model performance degrades over time due to changes in underlying data
   - C) When a model is transferred from one team to another
   - D) When multiple models are combined into an ensemble

## Short Answer Questions

6. **Compare and contrast CRISP-DM and IBM's Data Science Methodology. What are the key differences?**

7. **Explain the concept of "feature engineering" and provide two examples of feature engineering techniques.**

8. **Why is the data science methodology described as iterative rather than linear? Give an example of how feedback might lead to revisiting an earlier phase.**

9. **What is the difference between overfitting and underfitting? How might you detect each problem?**

10. **Explain the importance of the "Deployment" phase in a data science project. What key activities happen during this phase?**

## Practical Exercise

11. **Case Study: Retail Customer Churn Prediction**  
    A retail company wants to identify customers who are likely to stop shopping with them in the next 3 months.

    a) Outline the business understanding phase for this scenario. What are the key questions to ask?
    
    b) What data would you request for this project? List at least 5 potential data sources or features.
    
    c) Describe 3 data preparation steps you might need to take for this project.
    
    d) How would you evaluate the success of your churn prediction model? Which metrics would be most appropriate and why?

---

**Answers:**
1. C - Analytic Approach is a phase in IBM's methodology but not in CRISP-DM.
2. B - The Business Understanding phase is about defining the problem and objectives.
3. C - Data Preparation involves cleaning data, handling missing values, and outliers.
4. C - Evaluation focuses on determining if the model achieves the business objectives.
5. B - Model drift occurs when model performance degrades due to changes in data patterns.
6. CRISP-DM has 6 phases while IBM's methodology has 10 phases. IBM's methodology adds specific phases like Analytic Approach, Data Requirements, and Feedback that aren't explicitly called out in CRISP-DM. IBM's approach separates data collection from data understanding, while CRISP-DM combines them. Both are iterative, but IBM's methodology emphasizes the feedback loop more explicitly.
7. Feature engineering is the process of creating new features from existing data to improve model performance. Examples include: (1) Creating interaction terms (e.g., multiplying two features together), (2) Extracting date components (day of week, month, year) from a timestamp, (3) Creating categorical bins from continuous variables, (4) Text mining to extract sentiment scores from text data.
8. The data science methodology is iterative because findings in later stages often require revisiting earlier stages. For example, during modeling, we might discover that certain features aren't predictive, requiring us to go back to data preparation or even data collection to obtain better variables. Similarly, after deployment, model performance might degrade, requiring a return to the modeling or data preparation phase.
9. Overfitting occurs when a model learns the training data too well, including noise, resulting in poor generalization. It can be detected when performance is excellent on training data but poor on test data. Underfitting happens when a model is too simple to capture the underlying patterns, resulting in poor performance on both training and test data. It can be detected by observing high bias/error on training data.
10. The Deployment phase involves implementing the model in production environments where it can deliver value. Key activities include: integrating with existing systems, developing monitoring processes to track performance, planning for maintenance and updates, documenting the solution, training stakeholders on how to use and interpret results, and creating a feedback mechanism to capture information for future improvements.