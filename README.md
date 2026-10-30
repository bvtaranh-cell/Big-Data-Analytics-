# Diabetes Risk Analysis and Prediction Using Apache Spark

**Course:** SAT5165 – Big Data Analytics  
**Project Members:** Blessing Taranhike and Leona Chazanga

## Project Overview

This project uses Apache Spark and machine learning to analyze the CDC Diabetes Health Indicators dataset and identify health, demographic, and lifestyle factors associated with diabetes. A logistic regression model is developed using Spark MLlib to predict diabetes status.

The project also explores Spark performance under different worker configurations to understand how the number of workers affects execution time.

## Objectives

- Analyze factors associated with diabetes.
- Perform data preprocessing and descriptive statistical analysis using PySpark.
- Identify relationships between diabetes and selected health indicators using Pearson correlation.
- Develop a diabetes prediction model using Spark MLlib logistic regression.
- Evaluate model performance using classification metrics.
- Compare Spark execution performance under different worker configurations.

## Dataset

The project uses the **CDC Diabetes Health Indicators Dataset** from the UCI Machine Learning Repository.

[Access the dataset](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators)

- Original records: 253,680
- Predictor variables: 21
- Target variable: `Diabetes_binary`
- Final records after duplicate removal: 229,474

The target variable is binary:
- `0` – No Diabetes
- `1` – Diabetes

## Tools and Technologies

- Python
- Apache Spark (PySpark)
- Spark MLlib
- Pandas
- NumPy
- Matplotlib
- Google Colab

## Methodology

1. **Data Loading and Preprocessing:** Load the dataset, inspect data quality, check missing values, remove duplicates, and prepare the data for analysis.
2. **Descriptive Statistical Analysis:** Examine summary statistics and compare selected characteristics between diabetes categories.
3. **Correlation Analysis:** Use Pearson correlation to identify variables associated with diabetes status.
4. **Predictive Modeling:** Develop a logistic regression model using Spark MLlib with an 80/20 training and testing split.
5. **Model Evaluation:** Evaluate performance using accuracy, precision, recall, F1-score, AUC, and a confusion matrix.
6. **Spark Benchmarking:** Compare preprocessing, statistical analysis, and machine-learning execution times under different Spark worker configurations.

## Key Findings

The analysis identified the following variables as having the strongest positive correlations with diabetes status:

| Variable | Correlation |
|---|---:|
| General Health | 0.277 |
| High Blood Pressure | 0.254 |
| Difficulty Walking | 0.205 |
| BMI | 0.205 |
| High Cholesterol | 0.195 |

Individuals with diabetes also had a higher average BMI (31.96) compared with individuals without diabetes (28.10).

## Model Performance

The logistic regression model achieved the following recorded results:

| Metric | Result |
|---|---:|
| AUC | 0.809 |
| Accuracy | 85.2% |
| Weighted Precision | 81.8% |
| Weighted Recall | 85.2% |
| Weighted F1-score | 81.2% |

The model demonstrated reasonable overall performance but had low recall (14%) for the diabetes category, indicating difficulty identifying actual diabetes cases.

## Project Files

The repository includes:
- Main diabetes risk analysis and prediction notebook.
- Spark performance benchmarking notebook.
- Project documentation and supporting analysis.

## Conclusion

This project demonstrates the use of Apache Spark and machine learning to analyze population health data, identify factors associated with diabetes, and develop a predictive model. The findings highlight the importance of health indicators such as general health, high blood pressure, and BMI. Future improvements could explore additional machine-learning algorithms and techniques to address class imbalance and improve diabetes detection.

## References

- [UCI Machine Learning Repository – CDC Diabetes Health Indicators](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators)
- Zaharia, M., et al. (2016). *Apache Spark: A Unified Engine for Big Data Processing*. Communications of the ACM.
