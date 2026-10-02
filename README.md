# Practical-Statistics-for-Data-Scientist-Books

**Author:** Ruben Alfa Richie
**Date:** September 29, 2026  
**Course:** Machine Learning and Deep Learning  
**Assignment:** Individual Task - Code Reproduction + Theoretical Explanation

---

## 📚 Book Information

**Title:** Practical Statistics for Data Scientists: 50+ Essential Concepts Using R and Python  
**Authors:** Peter Bruce, Andrew Bruce, Peter Gedeck  
**Edition:** Second Edition  
**Publisher:** O'Reilly Media

---

## 📋 Chapter Summaries

### Chapter 1: Exploratory Data Analysis

**Overview:** The foundation of any data science project starts with exploring and understanding your data. This chapter introduces essential techniques for summarizing and visualizing data.

**What You'll Learn:**
- **Data Types**: Understanding numeric (continuous/discrete) vs categorical (binary/ordinal) data and why it matters for analysis
- **Location Estimates**: Measuring central tendency with mean, median, trimmed mean, and weighted mean. Learn when each is appropriate
- **Variability Measures**: Quantifying spread using variance, standard deviation, IQR, and MAD. Discover robust alternatives to standard deviation
- **Distribution Exploration**: Using histograms, density plots, and boxplots to understand data shape, skewness, and outliers
- **Correlation Analysis**: Measuring relationships between variables with Pearson and Spearman correlation
- **Categorical Data**: Analyzing frequency tables, bar charts, and contingency tables
- **Multivariate Exploration**: Exploring relationships between multiple variables using scatterplot matrices and grouped visualizations

**Key Takeaways:**
- Mean is sensitive to outliers; median is robust
- Standard deviation assumes normality; IQR works for any distribution
- Correlation measures linear relationships only and does not imply causation
- Always visualize your data before applying statistical methods

**Practical Applications:** Data quality checks, outlier detection, feature selection, understanding variable relationships

---

### Chapter 2: Data and Sampling Distributions

**Overview:** Understanding how samples relate to populations is crucial for statistical inference. This chapter covers sampling theory, the Central Limit Theorem, and fundamental probability distributions.

**What You'll Learn:**
- **Sampling Methods**: Random sampling vs biased sampling, and why quality matters more than quantity
- **Types of Bias**: Selection bias, survivorship bias, self-selection bias, and how to avoid them
- **Central Limit Theorem**: Why sample means follow a normal distribution regardless of the population distribution
- **Standard Error**: Measuring the precision of estimates and how it decreases with sample size
- **Bootstrap Resampling**: A powerful technique for estimating sampling distributions without mathematical formulas
- **Confidence Intervals**: Quantifying uncertainty in estimates
- **Key Distributions**:
  - **Normal**: The bell curve - foundation of classical statistics
  - **t-Distribution**: For small samples or unknown population variance
  - **Binomial**: Modeling success/failure experiments
  - **Poisson**: Counting rare events in fixed intervals
  - **Exponential**: Time between events
  - **Chi-Square & F**: For variance tests and ANOVA

**Key Takeaways:**
- A biased sample, no matter how large, gives biased results
- CLT is why normal-based inference works for most real-world data
- Bootstrap provides a modern, assumption-free approach to inference
- Choose distributions based on your data type and the question you're asking

**Practical Applications:** Survey design, A/B test planning, error estimation, sample size calculations

---

### Chapter 3: Statistical Experiments and Significance Testing

**Overview:** Learn how to design experiments and test hypotheses rigorously. This chapter covers the framework for determining whether observed effects are real or due to chance.

**What You'll Learn:**
- **A/B Testing**: The gold standard for online experiments - random assignment, control groups, and treatment effects
- **Hypothesis Testing Framework**: Null vs alternative hypotheses, Type I and Type II errors, statistical power
- **Permutation Tests**: Non-parametric resampling approach that works without distributional assumptions
- **p-Values**: What they mean (and don't mean), proper interpretation, and common misconceptions
- **t-Tests**: Comparing means between two groups (independent and paired)
- **ANOVA**: Comparing means across three or more groups using variance decomposition
- **Chi-Square Tests**: Testing independence between categorical variables
- **Multiple Testing Problem**: Why testing many hypotheses inflates false positives and how to correct it

**Key Takeaways:**
- p-value is NOT the probability that the null hypothesis is true
- Statistical significance ≠ practical importance
- Always establish your hypothesis and significance level before collecting data
- Multiple testing requires correction (Bonferroni, FDR) to control false positives
- Permutation tests are powerful alternatives when assumptions are questionable

**Practical Applications:** A/B testing websites, clinical trials, marketing campaign evaluation, quality control

---

### Chapter 4: Regression and Prediction

**Overview:** Regression is the workhorse of predictive modeling. This chapter teaches you to build, evaluate, and diagnose linear regression models.

**What You'll Learn:**
- **Simple Linear Regression**: Fitting a line to data using least squares, interpreting slope and intercept
- **Multiple Regression**: Building models with multiple predictors and understanding partial effects
- **Model Assessment**: R², adjusted R², RMSE, and MAE for measuring prediction quality
- **Cross-Validation**: Getting honest estimates of model performance using train/test splits and k-fold CV
- **Regression Diagnostics**:
  - Identifying outliers and influential points
  - Testing for heteroscedasticity (non-constant variance)
  - Checking linearity assumptions
  - Detecting multicollinearity
- **Model Selection**: Balancing complexity vs performance
- **Prediction Intervals**: Quantifying uncertainty in predictions

**Key Takeaways:**
- Training error always underestimates true prediction error
- Cross-validation is essential for honest performance estimates
- Check residual plots, not just R²
- Outliers and influential points can distort your entire model
- Never extrapolate beyond the range of your training data

**Practical Applications:** Price prediction, sales forecasting, resource planning, risk assessment

---

### Chapter 5: Classification

**Overview:** When your outcome is categorical, classification algorithms come into play. Learn to predict binary and multiclass outcomes and evaluate classifier performance.

**What You'll Learn:**
- **Logistic Regression**: Predicting probabilities using the logistic function, interpreting coefficients as odds ratios
- **Naive Bayes**: Probabilistic classifier based on Bayes' theorem - fast and effective for text classification
- **Discriminant Analysis**: Finding linear combinations of features that best separate classes
- **Confusion Matrix**: Understanding true/false positives/negatives
- **Performance Metrics**:
  - **Accuracy**: Overall correctness
  - **Precision**: Of predicted positives, how many are correct?
  - **Recall (Sensitivity)**: Of actual positives, how many did we catch?
  - **F1-Score**: Harmonic mean of precision and recall
  - **Specificity**: Of actual negatives, how many did we correctly identify?
- **ROC Curves & AUC**: Visualizing classifier performance across all thresholds
- **Imbalanced Data**: Techniques for handling rare class problems (undersampling, oversampling, SMOTE)

**Key Takeaways:**
- Accuracy is misleading for imbalanced data
- There's a precision-recall tradeoff controlled by the decision threshold
- ROC curves show performance across all possible thresholds
- AUC > 0.9 is excellent, > 0.8 is good, 0.5 is random guessing
- Always consider the cost of false positives vs false negatives

**Practical Applications:** Fraud detection, medical diagnosis, spam filtering, customer churn prediction

---

### Chapter 6: Statistical Machine Learning

**Overview:** Modern machine learning methods that go beyond simple linear models. Learn ensemble methods that power many production systems.

**What You'll Learn:**
- **K-Nearest Neighbors (KNN)**:
  - Instance-based learning - no training phase
  - Distance metrics and the importance of feature scaling
  - Choosing k: bias-variance tradeoff
- **Decision Trees**:
  - Recursive partitioning algorithm
  - Splitting criteria (Gini impurity, entropy)
  - Interpretability vs performance
  - Overfitting problem
- **Random Forests**:
  - Bagging: Bootstrap aggregating for variance reduction
  - Random feature selection decorrelates trees
  - Feature importance rankings
  - Superior performance and robustness
- **Boosting (Gradient Boosting)**:
  - Sequential learning - each tree corrects previous errors
  - XGBoost: state-of-the-art implementation
  - Regularization to prevent overfitting
- **Hyperparameter Tuning**: Grid search and cross-validation for optimal settings

**Key Takeaways:**
- Single trees overfit; ensembles (Random Forest, Boosting) don't
- Random Forests are hard to beat for tabular data
- Boosting often wins Kaggle competitions but requires careful tuning
- KNN requires scaled features and is slow at prediction time
- Always monitor train vs test performance to detect overfitting

**Practical Applications:** Credit scoring, recommendation systems, demand forecasting, anomaly detection

---

### Chapter 7: Unsupervised Learning

**Overview:** When you don't have labels, unsupervised learning finds hidden structure in data. Learn dimensionality reduction and clustering techniques.

**What You'll Learn:**
- **Principal Component Analysis (PCA)**:
  - Finding new coordinate system that captures maximum variance
  - Dimensionality reduction: 100 features → 2 components while retaining 95% of information
  - Scree plots and explained variance
  - Applications: visualization, noise reduction, feature engineering
- **K-Means Clustering**:
  - Partitioning data into k groups
  - Algorithm: assign points to centroids, update centroids, repeat
  - Elbow method for choosing optimal k
  - Limitations: assumes spherical clusters, sensitive to initialization
- **Hierarchical Clustering**:
  - Building a tree (dendrogram) of nested clusters
  - Agglomerative (bottom-up) approach
  - Linkage methods: single, complete, average, Ward
  - Cutting dendrograms at different heights for different k
- **Scaling Considerations**: Why standardization is crucial for distance-based methods

**Key Takeaways:**
- PCA is linear; for non-linear data, consider t-SNE or UMAP
- First 2-3 principal components often capture 70-90% of variance
- K-Means is fast and scalable but requires specifying k
- Hierarchical clustering provides a full tree structure but is computationally expensive
- Always validate clusters with domain knowledge - algorithms will always find clusters even in random data

**Practical Applications:** Customer segmentation, image compression, anomaly detection, exploratory data analysis, feature engineering

---

## 🛠️ Technical Setup

**Python Libraries Used:**
```python
numpy          # Numerical computing
pandas         # Data manipulation
matplotlib     # Visualization
seaborn        # Statistical visualization
scipy.stats    # Statistical functions
```

**Installation:**
```bash
pip install numpy pandas matplotlib seaborn scipy jupyter
```

**Running Notebooks:**
```bash
cd notebooks
jupyter notebook
```

---

## 📚 References

1. Bruce, P., Bruce, A., & Gedeck, P. (2020). *Practical Statistics for Data Scientists: 50+ Essential Concepts Using R and Python* (2nd ed.). O'Reilly Media.
2. Tukey, J. W. (1977). *Exploratory Data Analysis*. Addison-Wesley.
3. Donoho, D. (2017). 50 Years of Data Science. *Journal of Computational and Graphical Statistics*, 26(4), 745-766.

---

## 👤 Author

**Name:** Ruben Alfa Richie  
**GitHub:** [@rubenalfarichie](https://github.com/rubenalfarichie)  
**Course:** Machine Learning and Deep Learning  

**Repository:** https://github.com/rubenalfarichie/Practical-Statistics-for-Data-Scientists-Books

---
