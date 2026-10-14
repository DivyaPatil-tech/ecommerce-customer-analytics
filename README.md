# **E-Commerce Customer Analytics Using Machine Learning**

**Project Overview**

This project applies machine learning techniques to an e-commerce customer dataset to analyze customer spending, predict customer churn, identify customer segments, and discover product associations.

The project demonstrates four analytical approaches: regression, classification, clustering, and association rule mining.

**Business Problem**

E-commerce businesses need to understand customer purchasing behavior, identify customers who may churn, segment customers for targeted marketing, and discover products that are frequently purchased together.

This project explores how machine learning can support these business objectives.

**Objectives**

- Predict customer total spending using regression models.
- Classify customers based on churn status.
- Visualize classification performance using confusion matrices.
- Segment customers using K-Means clustering.
- Discover product associations using the Apriori algorithm.
- Compare model performance and summarize business insights.

**Dataset**

The dataset contains customer-related information, including:

- Age
- Annual income
- Spending score
- Total purchases
- Total spending
- Churn status
- Items bought

The "ChurnStatus" interpretation is assumed to be "1 = churned" and "0 = active". This assumption must be verified against the original dataset documentation.

**Technologies Used**

- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Mlxtend

**Methodology**

1. Data Cleaning and Exploratory Data Analysis

Inspect data types, missing values, duplicate records, statistical summaries, correlations, distributions, and potential outliers.

2. Regression

Compare Linear Regression, Decision Tree Regressor, and Random Forest Regressor using MAE, MSE, RMSE, and R².

3. Classification

Compare Logistic Regression, Decision Tree Classifier, and Random Forest Classifier using accuracy, precision, recall, F1-score, classification reports, and confusion matrices.

4. Clustering

Apply K-Means to standardized numerical customer features and analyze the characteristics of three initial customer segments.

5. Association Rule Mining

Apply Apriori to product transactions and examine support, confidence, and lift.

**Initial Results**

Linear Regression achieved the best initial regression results, with an MAE of approximately 403.10 and an R² score of 0.9922.

Decision Tree and Random Forest classification achieved 100% accuracy on the current test split. However, the dataset contains very few positive churn examples, so these results require further validation.

The clustering and association analyses identified exploratory customer segments and product co-occurrence patterns.

These results are preliminary and should not be interpreted as proof of real-world predictive performance.

**How to Run the Project**

1. Clone or download the repository.
2. Install the required Python libraries.
3. Place the dataset in the appropriate location if it is not included.
4. Open "ecommerce_customer_analytics.ipynb" in Jupyter Notebook or VS Code.
5. Run the notebook cells in order.

**Limitations**

- The churn-positive class is underrepresented.
- The regression results require investigation for possible target leakage.
- Three clusters were selected as an initial choice, not proven optimal.
- Association rules describe co-occurrence, not causation.
- Results may not generalize to new customers.

**Future Improvements**

- Validate the churn labels against the original data documentation.
- Evaluate models using additional data and appropriate cross-validation.
- Investigate potential target leakage.
- Explore improved methods for handling class imbalance.
- Validate customer segments and association rules on new transactions.

Author

Machine Learning Portfolio Project
