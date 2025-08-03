# Iris Flower Classification

A comprehensive classification project that identifies iris flower species based on morphological features using multiple machine learning algorithms.

## Objectives

- Classify iris flowers into three species using sepal and petal measurements
- Compare performance of six different classification algorithms
- Analyze feature relationships and identify optimal classification approach
- Evaluate model robustness through confusion matrices and classification metrics

## Dataset

The iris dataset contains 150 samples with 4 morphological features:
- **SepalLengthCm**: Length of sepal in centimeters
- **SepalWidthCm**: Width of sepal in centimeters
- **PetalLengthCm**: Length of petal in centimeters
- **PetalWidthCm**: Width of petal in centimeters

**Target Classes**: Iris-setosa, Iris-versicolor, Iris-virginica (50 samples each)

The dataset contains no missing values or duplicates, making it ideal for classification analysis.

## Methodology

### Exploratory Data Analysis
- Pairplot analysis revealed clear linear separability of Iris-setosa from other species
- Correlation analysis showed high correlation between petal length and width (r > 0.9)
- Outlier detection using box plots identified minimal outliers across features
- Perfect class balance with equal representation of all three species

### Preprocessing Strategy
- Applied label encoding to convert species names to numerical targets (0, 1, 2)
- Implemented stratified train-test split (70-30) to maintain class distribution
- Applied StandardScaler for feature normalization to ensure fair comparison across algorithms with different distance metrics

### Model Selection Rationale
Six algorithms were chosen to capture different classification approaches:

**Logistic Regression**: Linear probabilistic classifier using maximum likelihood estimation

**K-Nearest Neighbors**: Instance-based learning using local neighborhood voting

**Decision Tree**: Rule-based classifier creating interpretable decision boundaries

**Random Forest**: Ensemble method combining multiple decision trees with bootstrap aggregating

**Support Vector Machine**: Maximum margin classifier with linear kernel for optimal separation

**Naive Bayes**: Probabilistic classifier assuming feature independence with Gaussian distributions

### Evaluation Framework
- Used stratified sampling to ensure representative test sets
- Generated confusion matrices for detailed error analysis
- Evaluated using precision, recall, and F1-score for each class
- Calculated macro and weighted averages for overall performance assessment

## Results

| Model | Accuracy | Macro Avg Precision | Macro Avg Recall | Macro Avg F1-Score |
|-------|----------|---------------------|------------------|-------------------|
| Logistic Regression | 0.91 | 0.92 | 0.91 | 0.91 |
| K-Nearest Neighbors | 0.91 | 0.93 | 0.91 | 0.91 |
| Decision Tree | 0.91 | 0.91 | 0.91 | 0.91 |
| Random Forest | 0.89 | 0.90 | 0.89 | 0.89 |
| Support Vector Machine | 0.91 | 0.92 | 0.91 | 0.91 |
| Naive Bayes | 0.91 | 0.92 | 0.91 | 0.91 |

### Key Findings
- All models achieved perfect classification for Iris-setosa (100% precision and recall)
- Primary classification difficulty occurred between Iris-versicolor and Iris-virginica
- Logistic Regression and SVM demonstrated most consistent performance across all metrics
- Random Forest showed slightly lower performance despite being an ensemble method
- Feature standardization proved crucial for distance-based algorithms (KNN, SVM)

### Confusion Matrix Analysis
- Iris-setosa: Zero misclassifications across all models due to clear linear separability
- Iris-versicolor: Occasional misclassification as Iris-virginica in most models
- Iris-virginica: Some confusion with Iris-versicolor, particularly in Random Forest

## Conclusion

The analysis demonstrates that multiple algorithms can effectively classify iris species with over 89% accuracy. Logistic Regression and Support Vector Machine emerged as the optimal choices, achieving 91% accuracy with balanced precision and recall across all classes.

The perfect classification of Iris-setosa confirms the biological distinctiveness observed in exploratory analysis. The primary challenge lies in distinguishing between Iris-versicolor and Iris-virginica, which share similar morphological characteristics.

From a practical standpoint, the high correlation between petal measurements suggests potential for dimensionality reduction, while the consistent performance across diverse algorithms indicates the robustness of the feature set for species classification.

Logistic Regression is recommended for deployment due to its combination of high accuracy, interpretability, computational efficiency, and probabilistic output suitable for uncertainty quantification.
