# Machine Learning with Python

## Introduction to Machine Learning

Machine Learning is a subset of artificial intelligence that provides systems the ability to automatically learn and improve from experience without being explicitly programmed. The learning process begins with observations or data, such as examples, direct experience, or instruction, in order to look for patterns in data and make better decisions in the future based on the examples provided.

### Key Machine Learning Paradigms

1. **Supervised Learning**: Training on labeled data
   - Regression: Predicting continuous values
   - Classification: Predicting categorical values

2. **Unsupervised Learning**: Finding patterns in unlabeled data
   - Clustering: Grouping similar data points
   - Dimensionality Reduction: Reducing features while preserving information

3. **Reinforcement Learning**: Learning through interaction with environment

## Data Science Lifecycle for Machine Learning

1. **Problem Definition**
   - Define business objectives
   - Formulate problem as a machine learning task

2. **Data Collection**
   - Gather relevant data sources
   - Ensure data quality and relevance

3. **Data Preprocessing**
   - Handle missing values
   - Feature engineering
   - Data transformation and normalization
   - Train/test split

4. **Model Selection & Training**
   - Choose appropriate algorithms
   - Train models on data
   - Tune hyperparameters

5. **Evaluation**
   - Measure performance using appropriate metrics
   - Cross-validation to ensure generalizability

6. **Deployment & Monitoring**
   - Integrate model into production systems
   - Monitor and update as needed

## Regression Models

### Linear Regression

Linear regression establishes a linear relationship between input variables and a continuous output variable.

**Key Concepts**:
- **Simple Linear Regression**: One independent variable
- **Multiple Linear Regression**: Multiple independent variables
- **Ordinary Least Squares (OLS)**: Minimizing the sum of squared residuals
- **R-squared**: Coefficient of determination measuring model fit
- **Gradient Descent**: Optimization algorithm for finding coefficients

**Important Syntax**:
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)

# Coefficients and intercept
coefficients = model.coef_
intercept = model.intercept_
```

### Polynomial Regression

Extension of linear regression that captures nonlinear relationships by adding polynomial terms.

**Important Syntax**:
```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import Pipeline

steps = [
    ('polynomial', PolynomialFeatures(degree=2)),
    ('model', LinearRegression())
]

model = Pipeline(steps)
model.fit(X_train, y_train)
```

### Regularized Regression

Techniques to prevent overfitting in regression models by penalizing large coefficients.

**Types**:
- **Ridge Regression (L2)**: Adds squared magnitude of coefficients as penalty
- **Lasso Regression (L1)**: Adds absolute value of coefficients as penalty
- **Elastic Net**: Combines L1 and L2 regularization

**Important Syntax**:
```python
# Ridge Regression
from sklearn.linear_model import Ridge
ridge = Ridge(alpha=1.0)  # Alpha controls regularization strength

# Lasso Regression
from sklearn.linear_model import Lasso
lasso = Lasso(alpha=1.0)

# Elastic Net
from sklearn.linear_model import ElasticNet
elastic_net = ElasticNet(alpha=1.0, l1_ratio=0.5)  # l1_ratio controls L1 vs L2 balance
```

## Classification Models

### Logistic Regression

Despite its name, logistic regression is a classification model that predicts the probability of a binary outcome.

**Key Concepts**:
- **Sigmoid Function**: Maps predictions to probabilities between 0 and 1
- **Decision Boundary**: Threshold for classification (default: 0.5)
- **Cost Function**: Log loss or cross-entropy
- **Regularization**: L1 and L2 regularization to prevent overfitting

**Important Syntax**:
```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression(C=1.0, penalty='l2')  # C is inverse of regularization strength
model.fit(X_train, y_train)
predictions = model.predict(X_test)
probabilities = model.predict_proba(X_test)  # Probability estimates
```

### K-Nearest Neighbors (KNN)

A non-parametric algorithm that classifies instances based on majority vote of K nearest neighbors.

**Key Concepts**:
- **Distance Metrics**: Euclidean, Manhattan, Minkowski
- **K Value**: Number of neighbors to consider (odd numbers preferred)
- **Curse of Dimensionality**: Performance degrades in high-dimensional space
- **Feature Scaling**: Essential for distance-based algorithms

**Important Syntax**:
```python
from sklearn.neighbors import KNeighborsClassifier
model = KNeighborsClassifier(n_neighbors=5, metric='euclidean')
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

### Support Vector Machines (SVM)

Finds the optimal hyperplane that maximizes the margin between classes.

**Key Concepts**:
- **Margin**: Distance between hyperplane and closest data points (support vectors)
- **Kernel Trick**: Transforms data into higher dimensions for nonlinear classification
- **C Parameter**: Controls trade-off between smooth decision boundary and classifying training points correctly
- **Common Kernels**: Linear, Polynomial, RBF (Radial Basis Function), Sigmoid

**Important Syntax**:
```python
from sklearn.svm import SVC
model = SVC(C=1.0, kernel='rbf', gamma='auto')
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

### Naive Bayes

Probabilistic classifiers based on applying Bayes' theorem with strong independence assumptions between features.

**Types**:
- **Gaussian Naive Bayes**: For continuous data
- **Multinomial Naive Bayes**: For discrete counts (text classification)
- **Bernoulli Naive Bayes**: For binary feature vectors

**Important Syntax**:
```python
# Gaussian Naive Bayes
from sklearn.naive_bayes import GaussianNB
model = GaussianNB()

# Multinomial Naive Bayes
from sklearn.naive_bayes import MultinomialNB
model = MultinomialNB(alpha=1.0)  # Alpha is smoothing parameter
```

### Decision Trees

Tree-structured models where internal nodes represent feature tests and leaf nodes represent class labels.

**Key Concepts**:
- **Entropy**: Measure of impurity or randomness
- **Information Gain**: Reduction in entropy after splitting
- **Gini Index**: Alternative to entropy for measuring impurity
- **Pruning**: Reducing tree complexity to prevent overfitting

**Important Syntax**:
```python
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier(criterion='gini', max_depth=5)
model.fit(X_train, y_train)

# Visualizing the tree
from sklearn.tree import export_graphviz
export_graphviz(model, out_file='tree.dot', feature_names=X.columns)
```

### Random Forest

Ensemble learning method that constructs multiple decision trees and outputs the majority vote.

**Key Concepts**:
- **Bootstrap Aggregating (Bagging)**: Training trees on random subsets of data
- **Feature Randomness**: Considering random subsets of features when splitting nodes
- **Out-of-Bag (OOB) Error**: Estimate of model performance using samples not used in training
- **Feature Importance**: Ranking features by their contribution

**Important Syntax**:
```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(n_estimators=100, max_depth=5, random_state=42)
model.fit(X_train, y_train)
feature_importances = model.feature_importances_
```

## Deep Learning

### Neural Networks Basics

**Key Concepts**:
- **Neuron (Perceptron)**: Basic unit of computation
- **Activation Functions**: ReLU, Sigmoid, Tanh, Softmax
- **Weights and Biases**: Parameters learned during training
- **Forward Propagation**: Computing outputs from inputs
- **Backpropagation**: Computing gradients for updating weights
- **Loss Functions**: Measuring prediction error (MSE, Cross-entropy)

### Working with Keras

Keras is a high-level neural networks API that can run on top of TensorFlow, CNTK, or Theano.

**Important Syntax**:
```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Activation

# Create a sequential model
model = Sequential([
    Dense(64, activation='relu', input_shape=(784,)),
    Dense(64, activation='relu'),
    Dense(10, activation='softmax')
])

# Compile the model
model.compile(optimizer='adam',
              loss='categorical_crossentropy',
              metrics=['accuracy'])

# Model summary
model.summary()

# Train the model
history = model.fit(X_train, y_train, 
                   validation_split=0.2,
                   epochs=10, 
                   batch_size=32)

# Evaluate the model
model.evaluate(X_test, y_test)
```

### Convolutional Neural Networks (CNNs)

Specialized neural networks for processing structured grid data like images.

**Key Components**:
- **Convolutional Layer**: Applies filters to detect features
- **Pooling Layer**: Reduces spatial dimensions
- **Fully Connected Layer**: Makes final predictions

### MNIST Dataset with Keras

The MNIST dataset is a common benchmark in machine learning for handwritten digit recognition.

**Key Processing Steps**:
1. Load data
2. Reshape and normalize images
3. Convert labels to one-hot encoding
4. Build, train, and evaluate model

## Clustering

### K-Means Clustering

Partitioning observations into K clusters where each observation belongs to the cluster with the nearest mean.

**Key Concepts**:
- **Centroids**: Center points of clusters
- **Inertia**: Sum of squared distances to closest centroid
- **Elbow Method**: Technique to find optimal K value
- **Silhouette Score**: Measure of how similar objects are to their cluster vs other clusters

**Important Syntax**:
```python
from sklearn.cluster import KMeans
model = KMeans(n_clusters=3, random_state=42)
model.fit(X)
labels = model.labels_
centroids = model.cluster_centers_
```

### Hierarchical Clustering

Builds a hierarchy of clusters by recursively merging or splitting clusters.

**Types**:
- **Agglomerative**: Bottom-up approach, starts with each data point as a cluster
- **Divisive**: Top-down approach, starts with all data in one cluster

**Key Concepts**:
- **Linkage Methods**: Single, Complete, Average, Ward
- **Dendrogram**: Tree diagram showing hierarchical clustering

**Important Syntax**:
```python
from sklearn.cluster import AgglomerativeClustering
model = AgglomerativeClustering(n_clusters=3, linkage='ward')
labels = model.fit_predict(X)

# Creating a dendrogram
from scipy.cluster.hierarchy import dendrogram, linkage
Z = linkage(X, method='ward')
dendrogram(Z)
```

### DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

Clusters points based on density and can find arbitrarily shaped clusters.

**Key Concepts**:
- **Core Point**: Point with at least `min_samples` points within `eps` distance
- **Border Point**: Point within `eps` of a core point but not a core point itself
- **Noise Point**: Point that is neither a core nor a border point
- **Advantages**: No need to specify number of clusters; can find arbitrarily shaped clusters

**Important Syntax**:
```python
from sklearn.cluster import DBSCAN
model = DBSCAN(eps=0.5, min_samples=5)
labels = model.fit_predict(X)
```

## Evaluation Metrics

### For Regression

1. **Mean Absolute Error (MAE)**: Average absolute differences between predictions and actual values
2. **Mean Squared Error (MSE)**: Average squared differences between predictions and actual values
3. **Root Mean Squared Error (RMSE)**: Square root of MSE
4. **R-squared (R²)**: Proportion of variance explained by the model

**Important Syntax**:
```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import numpy as np

mae = mean_absolute_error(y_true, y_pred)
mse = mean_squared_error(y_true, y_pred)
rmse = np.sqrt(mse)
r2 = r2_score(y_true, y_pred)
```

### For Classification

1. **Accuracy**: Proportion of correct predictions
2. **Precision**: Proportion of positive identifications that were actually correct
3. **Recall (Sensitivity)**: Proportion of actual positives correctly identified
4. **F1-Score**: Harmonic mean of precision and recall
5. **Confusion Matrix**: Table showing true positives, false positives, true negatives, false negatives
6. **ROC Curve**: Receiver Operating Characteristic curve
7. **AUC**: Area Under the ROC Curve

**Important Syntax**:
```python
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score
from sklearn.metrics import confusion_matrix, roc_curve, auc

accuracy = accuracy_score(y_true, y_pred)
precision = precision_score(y_true, y_pred)
recall = recall_score(y_true, y_pred)
f1 = f1_score(y_true, y_pred)

# Confusion matrix
cm = confusion_matrix(y_true, y_pred)

# ROC curve and AUC
fpr, tpr, thresholds = roc_curve(y_true, y_pred_proba)
roc_auc = auc(fpr, tpr)
```

## Model Improvement Techniques

### Cross-Validation

Technique for assessing model performance by partitioning data into subsets for training and validation.

**Types**:
- **K-Fold**: Splits data into k equal folds, trains on k-1 folds and validates on the remaining fold
- **Stratified K-Fold**: Maintains class distribution in each fold
- **Leave-One-Out**: Uses one observation for validation and rest for training

**Important Syntax**:
```python
from sklearn.model_selection import cross_val_score, KFold, StratifiedKFold

# Simple cross-validation
scores = cross_val_score(model, X, y, cv=5)

# Custom K-Fold
kfold = KFold(n_splits=5, shuffle=True, random_state=42)
scores = cross_val_score(model, X, y, cv=kfold)

# Stratified K-Fold (for classification)
skfold = StratifiedKFold(n_splits=5, shuffle=True, random_state=42)
scores = cross_val_score(model, X, y, cv=skfold)
```

### Hyperparameter Tuning

Process of finding the optimal set of hyperparameters for a learning algorithm.

**Methods**:
- **Grid Search**: Exhaustive search over specified parameter values
- **Random Search**: Random sampling of parameter values
- **Bayesian Optimization**: Uses probabilistic model to find optimal parameters

**Important Syntax**:
```python
from sklearn.model_selection import GridSearchCV, RandomizedSearchCV

# Grid Search
param_grid = {
    'n_estimators': [100, 200, 300],
    'max_depth': [None, 5, 10],
    'min_samples_split': [2, 5, 10]
}
grid_search = GridSearchCV(model, param_grid, cv=5, scoring='accuracy')
grid_search.fit(X_train, y_train)
best_params = grid_search.best_params_
best_model = grid_search.best_estimator_

# Random Search
from scipy.stats import randint
param_dist = {
    'n_estimators': randint(100, 500),
    'max_depth': randint(3, 20),
    'min_samples_split': randint(2, 20)
}
random_search = RandomizedSearchCV(model, param_dist, n_iter=20, cv=5)
random_search.fit(X_train, y_train)
```

### Feature Engineering

Process of creating new features or transforming existing ones to improve model performance.

**Techniques**:
- **Feature Transformation**: Log, square root, polynomial features
- **Feature Scaling**: Standardization, Normalization
- **Encoding Categorical Variables**: One-hot encoding, Label encoding
- **Feature Creation**: Creating new features from existing ones
- **Dimensionality Reduction**: PCA, t-SNE

**Important Syntax**:
```python
from sklearn.preprocessing import StandardScaler, OneHotEncoder, PolynomialFeatures
from sklearn.compose import ColumnTransformer
from sklearn.pipeline import Pipeline
from sklearn.decomposition import PCA

# Feature scaling
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# One-hot encoding
encoder = OneHotEncoder(sparse=False)
X_encoded = encoder.fit_transform(X_categorical)

# Column transformer for mixed data types
preprocessor = ColumnTransformer(
    transformers=[
        ('num', StandardScaler(), numeric_features),
        ('cat', OneHotEncoder(), categorical_features)
    ])

# Dimensionality reduction with PCA
pca = PCA(n_components=2)
X_reduced = pca.fit_transform(X_scaled)
```

## Project Workflow

Typical workflow for machine learning projects:

1. **Data Exploration and Analysis**
   - Visualize data distributions
   - Check for missing values and outliers
   - Explore relationships between features

2. **Data Preprocessing**
   - Clean data (handle missing values, outliers)
   - Transform features (scaling, encoding)
   - Create new features if necessary

3. **Modeling**
   - Split data into train/test sets
   - Select appropriate algorithms
   - Train models and tune hyperparameters

4. **Evaluation**
   - Assess performance using appropriate metrics
   - Use cross-validation for robust evaluation
   - Compare multiple models

5. **Deployment**
   - Save trained model
   - Create application interface (web app, API, etc.)
   - Monitor model performance in production

### Saving and Loading Models

**Using pickle**:
```python
import pickle

# Save model
with open('model.pkl', 'wb') as file:
    pickle.dump(model, file)

# Load model
with open('model.pkl', 'rb') as file:
    loaded_model = pickle.load(file)
```

**Using joblib** (better for large NumPy arrays):
```python
from joblib import dump, load

# Save model
dump(model, 'model.joblib')

# Load model
loaded_model = load('model.joblib')
```

## Common Applications

1. **Car Price Prediction (Regression)**
   - Predict used car prices based on features like make, model, year, mileage
   - Typical features: year, kilometers_driven, fuel_type, transmission, engine capacity, etc.

2. **Customer Churn Prediction (Classification)**
   - Predict which customers are likely to leave a service
   - Typical features: usage patterns, customer demographics, service duration, etc.

3. **Credit Card Approval Prediction (Classification)**
   - Predict whether an application for a credit card will be approved
   - Typical features: income, debt, credit history, employment status, etc.

4. **Medical Insurance Cost Prediction (Regression)**
   - Predict healthcare costs based on patient information
   - Typical features: age, BMI, smoking status, region, number of dependents, etc.

5. **Digit Recognition (Image Classification)**
   - Classify handwritten digits using MNIST dataset
   - Uses neural networks with image preprocessing

6. **Customer Segmentation (Clustering)**
   - Group customers based on purchasing behavior
   - Identify market segments for targeted marketing
   - Typical features: purchase frequency, monetary value, recency, etc.

## References and Resources

1. ML Specialization, Coursera by Andrew Ng
2. Hands-on Machine Learning Book by Aurélien Géron
3. ML Zoomcamp, GitHub by Alexey Grigorev
4. ML Course, Kaggle by Ahmed Abul-Kheir