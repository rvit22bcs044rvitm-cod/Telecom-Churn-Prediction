# Customer Churn Prediction (End-to-End ML Pipeline)

##  Problem Statement
Customer churn is a critical challenge in the Telecom industry. This project aims to build a high-performance classification model to predict which customers are likely to leave based on their usage patterns, contract types, and demographics.

##  Technical Workflow
1. **Data Preprocessing**: Handled missing values in `TotalCharges` and performed IQR-based outlier capping.
2. **EDA**: Visualized key drivers such as Tenure vs. Churn and Contract Type influence.
3. **Feature Engineering**: Applied One-Hot Encoding and Label Encoding for categorical data.
4. **Data Integrity**: Implemented a strict **Zero-Leakage** strategy by splitting data before Scaling and SMOTE.
5. **Class Imbalance**: Used **SMOTE** to balance the training set.
6. **Model Selection**: Evaluated 7 models (Logistic Regression, KNN, SVC, Decision Tree, Random Forest, XGBoost, and Gradient Boosting).

## Key Results
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| **Gradient Boosting** | **78.1%** | **0.58** | **0.65** | **0.61** | **0.84** |

### Why Gradient Boosting?
While XGBoost showed higher accuracy, **Gradient Boosting** was selected as the final model due to its superior **Recall (0.65)**. In churn prediction, identifying potential churners (Recall) is more valuable than overall accuracy.

##  Business Recommendations
- **Contract Strategy**: Transition Month-to-Month users to long-term contracts via targeted discounts.
- **Tech Support**: Bundle technical support for Fiber Optic users to reduce friction.
- **Proactive Retention**: Focus on customers with high monthly charges in their first 12 months.

##  How to Run
1. Clone the repo.
2. Install dependencies: `pip install -r requirements.txt`.
3. Open `Customer_Churn_Prediction.ipynb` in Jupyter or Colab.
