# OIBSIP
Oasis InfoByte Internship | Task 1
Iris Flower Classification


## Objective

The objective of this project is to apply supervised machine learning techniques to classify iris flowers into one of three species: *Setosa*, *Versicolor*, and *Virginica* based on four numerical features: sepal length, sepal width, petal length, and petal width. The goal is to build a reliable classification model by evaluating and comparing different algorithms using key performance metrics.

## Tools and Technologies

**Python**
**Jupyter Notebook**
**Libraries:**
`pandas`, `numpy` for data manipulation
`matplotlib`, `seaborn` for exploratory data analysis and visualization
`scikit-learn` for preprocessing, model development, and evaluation

## Project Workflow

### Data Understanding and Exploration

The dataset used consists of 150 instances, each labeled with one of the three iris species.
Initial inspection revealed no missing or duplicated entries.
Exploratory Data Analysis (EDA) included:

• Distribution analysis of features using boxplots to check for outliers
• Pair plots to examine relationships between features and species separability
• Correlation heatmap to identify strongly correlated features (notably, petal length and petal width were highly correlated and informative for classification)

### Data Preparation

The target variable (species) was label-encoded for compatibility with scikit-learn classifiers.
Features were standardized using `StandardScaler` to ensure fair comparison across models sensitive to feature scale.
Data was split into training and test sets using a 70/30 ratio with stratification to preserve class distribution.

### Model Development and Evaluation

Six classification algorithms were implemented:

• Logistic Regression
• K-Nearest Neighbors (KNN)
• Decision Tree
• Random Forest
• Support Vector Machine (SVM)
• Naive Bayes

Each model was trained on the same training data and evaluated on the same test set. Performance was assessed using the following metrics:

• Precision: The proportion of positive identifications that were actually correct
• Recall: The proportion of actual positives that were identified correctly
• F1-score: The harmonic mean of precision and recall, providing a balance between the two
• Confusion Matrix: Used to visualize the performance of each model across the three classes

## Results and Interpretation

Below is a summary of performance across the models on the test set (15 samples per class):

**Logistic Regression**
Achieved strong performance across all species, especially in balancing recall and precision

**K-Nearest Neighbors**
Performed well on *Setosa* and *Versicolor*, but underperformed on *Virginica*

**Decision Tree**
Showed uniform performance across all classes, with solid recall but no significant advantage over simpler models

**Random Forest**
Showed slight decline in recall for *Virginica*, suggesting some overfitting or misclassification

**SVM (Linear Kernel)**
Mirrored Logistic Regression's performance, showing high generalization capability

**Naive Bayes**
Performed competitively despite its simplicity, indicating that class distributions were well-separated

All models achieved macro-averaged F1-scores around 0.91, with Logistic Regression, SVM, and Naive Bayes providing the most balanced performance across species.

## Conclusion

The classification task on the Iris dataset was successfully executed using a range of supervised learning algorithms. Despite the simplicity of the dataset, it provided a useful benchmark for comparing model behavior. Logistic Regression and Support Vector Machine demonstrated the most reliable and interpretable performance. Given their balance of precision and recall across all classes, these models are most appropriate for deployment in real-world classification scenarios involving similar datasets.

Further steps could include cross-validation for more robust evaluation, hyperparameter tuning for the tree-based models, and exploration of dimensionality reduction techniques such as PCA to visualize decision boundaries.

