E-Commerce Customer Analytics Using Machine Learning

1. Project Overview

This project applies machine learning techniques to an e-commerce customer dataset to analyze customer spending, predict customer churn, identify customer segments, and discover product purchasing associations.

The objective is to demonstrate how machine learning can support data-driven business decisions in customer analytics.

2. Business Problem

E-commerce businesses need to understand customer purchasing behavior, identify customers who may leave, segment customers based on their characteristics, and discover products that are frequently purchased together.

This project explores four machine learning tasks to address these business questions.

3. Project Objectives

- Predict customer spending using regression models.
- Predict customer churn using classification models.
- Segment customers using K-Means clustering.
- Discover product associations using association rule mining.
- Compare model performance using appropriate evaluation metrics.

4. Dataset Description

The project uses a programmatically generated synthetic dataset containing 1,000 rows and 8 columns.

Feature| Description
CustomerID| Customer identifier
Age| Customer age
AnnualIncome| Annual income
SpendingScore| Customer spending score
TotalPurchases| Total number of purchases
ChurnStatus| Customer churn indicator
TotalSpent| Total spending amount
ItemsBought| Comma-separated list of purchased products

The dataset is intended for educational and portfolio purposes. It does not establish real-world business performance.

5. Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- MLxtend
- Jupyter Notebook

6. Methodology

Exploratory Data Analysis (EDA)

- Inspected dataset structure, data types, missing values, and duplicate records.
- Examined distributions using histograms and count plots.
- Analyzed relationships using scatter plots, correlation analysis, and box plots.

Regression — Predicting Customer Spending

Models evaluated:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

Evaluation metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Classification — Predicting Customer Churn

Models evaluated:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Clustering — Customer Segmentation

K-Means clustering was applied to scaled customer features, using three clusters as an initial segmentation choice.

The resulting groups were examined using customer characteristics such as annual income, spending score, and purchase frequency.

Association Rule Mining — Product Associations

Apriori and association rules were used to identify relationships between products purchased together.

The analysis used:

- Support
- Confidence
- Lift

7. Results

Regression Results

Model| MAE| RMSE| R² Score
Linear Regression| 403.10| 499.10| 0.9922
Decision Tree Regressor| 1,006.24| 1,295.24| 0.9476
Random Forest Regressor| 624.44| 802.53| 0.9799

Linear Regression achieved the best results on the initial test split. The high R² score requires further validation before the model can be considered reliable for unseen real-world data.

Classification Results

Model| Accuracy| Churn Precision| Churn Recall| Churn F1-score
Logistic Regression| 99%| 1.00| 0.50| 0.67
Decision Tree| 100%| 1.00| 1.00| 1.00
Random Forest| 100%| 1.00| 1.00| 1.00

Decision Tree and Random Forest achieved identical results on the current test set. Random Forest is a candidate for further validation, not a proven superior model.

The test set contains only four churn cases, so these metrics are not sufficient to establish generalization performance.

8. Key Findings

- Spending score showed a strong positive correlation with total spending.
- Total purchases showed a moderate positive correlation with total spending.
- Customer groups displayed different spending scores and purchasing patterns.
- Association rules revealed product combinations with lift values greater than 1 in the analyzed dataset.

These findings describe the synthetic dataset and should not be interpreted as conclusions about actual e-commerce customers.

9. Project Structure

ecommerce-customer-analytics/
├── ecommerce_customer_analytics.ipynb
├── ecommerce_customer_analytics_clean.csv
├── ecommerce_multitask_dataset.csv
├── README.md
├── requirements.txt
├── .gitignore
└── reports/
    ├── regression_model_comparison.csv
    ├── classification_model_comparison.csv
    └── association_rules.csv

10. How to Run the Project

1. Clone or download this repository.

2. Install the required dependencies:
   
   pip install -r requirements.txt

3. Open the notebook in Jupyter:
   
   jupyter notebook ecommerce_customer_analytics.ipynb

4. Ensure the dataset path in the notebook points to the CSV file in the project directory.

5. Run the notebook cells in order.

11. Limitations

- The dataset is synthetic and may not represent real customer behavior.
- The classification dataset is imbalanced, with only 22 churn cases among 1,000 records.
- The classification test set contains only four churn cases.
- The regression results require further investigation for possible target leakage and validation on independent data.
- The choice of three K-Means clusters was an initial choice, not a validated optimal number.
- Association rules indicate patterns, not causal relationships.

12. Future Improvements

- Validate models using repeated stratified cross-validation and appropriate evaluation metrics.
- Investigate the synthetic data-generation process and potential target leakage.
- Test model performance on an independent dataset.
- Evaluate alternative customer segmentation choices.
- Develop a customer analytics dashboard.
- Explore personalized product recommendations.

13. Conclusion

This project demonstrates an end-to-end introductory customer analytics workflow using regression, classification, clustering, and association rule mining.

It provides a foundation for further experimentation with customer behavior analysis and machine learning model evaluation.

Author

Divya Patil

GitHub: https://github.com/DivyaPatil-tech
