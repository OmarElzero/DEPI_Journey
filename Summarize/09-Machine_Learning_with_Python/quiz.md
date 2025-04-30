# Machine Learning with Python Quiz

## Multiple Choice Questions

1. Which of the following is NOT a type of supervised learning?
   - a) Classification
   - b) Regression
   - c) Clustering
   - d) Support Vector Machines

2. In machine learning, what does the term "overfitting" refer to?
   - a) When a model performs well on training data but poorly on unseen data
   - b) When a model is too simple to capture the underlying pattern in the data
   - c) When the model training takes too much time
   - d) When the data preprocessing is incomplete

3. Which metric would be most appropriate for evaluating a regression model?
   - a) Accuracy
   - b) F1-score
   - c) Mean Squared Error (MSE)
   - d) Confusion Matrix

4. What is the purpose of the train_test_split function in scikit-learn?
   - a) To split the dataset into training and validation sets
   - b) To divide the features and target variables
   - c) To separate categorical and numerical features
   - d) To divide data into batches for neural network training

5. Which algorithm is based on the principle of "maximum margin classifier"?
   - a) Logistic Regression
   - b) Support Vector Machine
   - c) K-Means
   - d) Decision Tree

6. What is the primary purpose of feature scaling in machine learning models?
   - a) To improve model interpretability
   - b) To ensure features with larger ranges don't dominate those with smaller ranges
   - c) To convert categorical variables into numerical representations
   - d) To reduce the number of features in the dataset

7. In K-means clustering, what does the "K" represent?
   - a) The number of features in the dataset
   - b) The number of clusters to form
   - c) The number of iterations to perform
   - d) The kernel function to use

8. Which technique is used to prevent a decision tree from becoming too complex and overfitting?
   - a) Boosting
   - b) Bagging
   - c) Pruning
   - d) Stacking

9. What is the primary difference between L1 and L2 regularization?
   - a) L1 can lead to sparse models while L2 typically doesn't
   - b) L1 is only used for classification while L2 is for regression
   - c) L1 works with neural networks while L2 doesn't
   - d) L1 is computationally faster than L2

10. Which of the following is an ensemble learning method?
    - a) Linear Regression
    - b) Random Forest
    - c) K-Means
    - d) Principal Component Analysis

11. What does the C parameter control in a Support Vector Machine?
    - a) The learning rate
    - b) The number of clusters
    - c) The trade-off between smooth decision boundary and classifying training points correctly
    - d) The kernel type

12. In neural networks, which activation function outputs values between 0 and 1?
    - a) ReLU
    - b) Tanh
    - c) Sigmoid
    - d) Softmax

13. Which metric is best for evaluating imbalanced classification problems?
    - a) Accuracy
    - b) F1-score
    - c) Mean Squared Error
    - d) R-squared

14. What is the purpose of cross-validation in machine learning?
    - a) To speed up model training
    - b) To provide a more reliable estimate of model performance
    - c) To automatically select the best features
    - d) To visualize model predictions

15. What does DBSCAN stand for?
    - a) Density-Based Spatial Clustering of Applications with Noise
    - b) Decision-Based System for Classification and Numerical Analysis
    - c) Dynamic Binary Search for Clustering Analysis and Normalization
    - d) Deep Bayesian Systems for Complex Algorithmic Networks

## Short Answer Questions

1. Explain the difference between supervised and unsupervised learning. Give an example of each.

2. What is the bias-variance tradeoff in machine learning? How does model complexity relate to this tradeoff?

3. Describe the process of hyperparameter tuning and why it's important in machine learning.

4. Explain how the Random Forest algorithm works and why it often performs better than a single decision tree.

5. What is the purpose of a validation set in machine learning? How is it different from a test set?

6. Explain the concept of gradient descent and its role in training machine learning models.

7. What are the advantages and disadvantages of using deep learning compared to traditional machine learning algorithms?

8. Describe the difference between bagging and boosting as ensemble methods. Give an example of each.

9. What is the purpose of a confusion matrix? Explain what true positives, false positives, true negatives, and false negatives represent.

10. Explain the concept of feature importance and how it can be calculated in a Random Forest model.

## Practical Exercises

1. You are given a dataset about housing prices with features like square footage, number of bedrooms, location, etc. Write the Python code to:
   - Split the data into training and test sets
   - Create a pipeline for preprocessing (scaling numerical features and encoding categorical features)
   - Train a linear regression model
   - Evaluate the model using appropriate metrics

2. You have a dataset of customer information and want to predict whether a customer will churn (leave the service). The target variable is binary (churn/no churn). Write Python code to:
   - Handle any missing values in the dataset
   - Perform feature selection
   - Train a logistic regression model
   - Calculate the model's accuracy, precision, recall, and F1-score
   - Generate a ROC curve and calculate the AUC

3. You have an unlabeled dataset of customer purchasing behavior. Write Python code to:
   - Preprocess and scale the data
   - Determine the optimal number of clusters using the elbow method
   - Perform K-means clustering
   - Visualize the results
   - Interpret the characteristics of each cluster

4. Create a simple neural network using Keras for classifying handwritten digits from the MNIST dataset:
   - Load and preprocess the data
   - Create a sequential model with appropriate layers
   - Compile and train the model
   - Evaluate its performance
   - Make predictions on new samples

5. Implement a cross-validation strategy for a Random Forest model:
   - Set up k-fold cross-validation
   - Define a parameter grid for hyperparameter tuning
   - Perform grid search with cross-validation
   - Report the best parameters and their corresponding scores
   - Train the final model with the best parameters

## Data Science Scenario Questions

1. A company wants to predict customer lifetime value. They have historical data about customer demographics, purchasing history, and previous customer lifetime values. Describe your approach to building a predictive model, including data preprocessing, algorithm selection, and evaluation methods.

2. You've built a classification model that achieves 98% accuracy on your dataset. However, the precision and recall are very low for the minority class. What might be happening here, and how would you address this issue?

3. Your team has deployed a machine learning model in production, but after a few months, its performance starts to degrade. What could be causing this issue, and how would you monitor and address model degradation?

4. You need to build a recommendation system for an e-commerce website. Compare and contrast content-based filtering and collaborative filtering approaches. Which approach would you choose and why?

5. A non-technical stakeholder asks why your model made a specific prediction for a customer. Explain how you would approach model interpretability and what techniques you might use to help stakeholders understand the model's decision-making process.

## Answers to Multiple Choice Questions

1. c) Clustering (it's an unsupervised learning technique)
2. a) When a model performs well on training data but poorly on unseen data
3. c) Mean Squared Error (MSE)
4. a) To split the dataset into training and validation sets
5. b) Support Vector Machine
6. b) To ensure features with larger ranges don't dominate those with smaller ranges
7. b) The number of clusters to form
8. c) Pruning
9. a) L1 can lead to sparse models while L2 typically doesn't
10. b) Random Forest
11. c) The trade-off between smooth decision boundary and classifying training points correctly
12. c) Sigmoid
13. b) F1-score
14. b) To provide a more reliable estimate of model performance
15. a) Density-Based Spatial Clustering of Applications with Noise