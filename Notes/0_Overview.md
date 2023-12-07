# Overview

## Machine Learning Pipeline: General

![](..%2Ffiles%2Foverview%2Fml_pipeline_overview.png)

### Feature Engineering

- Problems in incoming data
  - **Missing Data:** Missing Values within a variable.
  - **Labels:** Strings in Categorical Variables
  - **Distribution:** Normal vs Skewed
  - **Outliers:** Unusual or unexpected values.

#### Missing Data
- Missing Values for certain observations.
- Affects all Machine Learning Models.

#### Labels in Categorical Variables
- Cardinality: High number of labels.
- Rare Labels: Infrequent Categories
- Categories: Strings

#### Distributions

- Better Spread of values may benefit performance.

#### Outliers

- Few Machine Learning Models are sensitive to outliers eg, Linear Regression, AdaBoost.

#### Scale of Feature Magnitude

- Machine Learning Models sensitive to a feature scale:
  - Linear and Logistic Regression.
  - Neural Networks.
  - Support Vector Machines.
  - KNN.
  - K-Means Clustering.
  - Linear Discriminative Analysis(LDA).
  - Principal Component Analysis.
- Tree Based ML Models insensitive to feature scale:
  - Classification and Regression Trees.
  - Random Forests.
  - Gradient Boosted Trees.

### Feature Engineering Techniques

- Missing Data Imputation Techniques.
  - Numerical Variables
    - Mean/Median Imputation
    - Arbitrary value Imputation
    - End of tail Imputation
  - Categorical Variables
    - Frequent Category Imputation
    - Adding a 'missing' category.
  - Both
    - Complete Case Analysis
    - Adding a 'missing' indicator
    - Random Sample Imputation
- Categorical Encoding Techniques
  - Traditional Techniques
    - One hot encoding
    - Count/frequency encoding
    - Ordinal/Label encoding
  - Monotonic Relationship
    - Ordered Label encoding
    - Mean encoding
    - Weight of evidence
  - Alternative techniques
    - Binary encoding
    - Feature hashing
    - Others
- Rare Labels Encoding Techniques
  - One hot encoding of frequent categories
  - Grouping of rare categories
- Distributions (Transform skewed to Gaussian for Continuous)
  - Mathematical transformation
    - Logarithmic
    - Exponential
    - Reciprocal
    - Box-Cox
    - Yeo-Johnson
  - Discretisation
    - Unsupervised
      - Equal-Width
      - Equal-Frequency
      - K Means
    - Supervised
      - Decision Trees
- Outliers
  - Discretisation
  - Capping/Censoring
  - Truncation
- Variable Magnitude
  - Scaling Methods
    - Standardisation
    - Mean Normalisation
    - Scaling to maximum and minimum
    - Scaling to absolute maximum
    - Scaling to median and quantiles
    - Scaling to unit norm.

### Feature Selection

- Refers to algorithms/procedures that allow us to identify the best subset of features from all features available in the dataset.
- Importance of Feature Selection:
  - Simple Models are easier to interpret.
  - Shorter training times.
  - Enhanced generalization by reducing overfitting.
  - Easier to implement by software developers -> Model Production.
  - Reduced risk of data errors during model use.
  - Data redundancy.
- Reducing features for model deployment.
  - Smaller json messages sent over to the model.
    - Json messages contain only the necessary variables/inputs.
  - Less lines of code for error handling.
    - Error handlers need to be written for each variable/input.
  - Less information to log.
  - Less feature engineering code.
- Variable Redundancy
  - **Constant variable:** Only 1 value per variable.
  - **Quasi-constant variables:** >99% of observations show same value.
  - **Duplication:** Same variable multiple times in the dataset.
  - **Correlation:** Correlated variables provide the same information.