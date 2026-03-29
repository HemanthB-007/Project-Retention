# 📉 Project Retention: AI-Driven Customer Churn Predictor

**Project Retention** is a machine learning pipeline designed to predict customer churn in subscription-based services. By analyzing demographic and behavioral data, the AI identifies high-risk customers before they cancel, allowing businesses to take proactive retention measures. 

This project emphasizes **Recall and F1-Score**, prioritizing the identification of churning customers over standard overall accuracy.

## 🧠 AI & Machine Learning Methodology

The core engine evaluates three distinct classification algorithms to find the optimal balance between predicting false positives (wasted retention budget) and false negatives (lost customers).

* **XGBoost (Champion Model):** Utilized for its superior handling of non-linear data and built-in feature importance tracking. Tuned with `scale_pos_weight` to handle class imbalance.
* **Random Forest:** Deployed as a robust ensemble baseline with `class_weight='balanced'`.
* **Logistic Regression:** Used as a linear baseline, requiring standard scaling of features for accurate gradient descent.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** Scikit-Learn, XGBoost, Pandas, NumPy
* **Environment:** Jupyter Notebook / Google Colab
* **Concepts:** Supervised Learning (Binary Classification), Feature Engineering, Class Imbalance Handling, Evaluation Metrics (Precision, Recall, F1-Score).

## 📊 Dataset & Features
The model runs on a 10,000-record dataset featuring key telecom/SaaS metrics:
* `Tenure_Months`: How long the customer has been active.
* `Monthly_Charges`: Revenue per user.
* `Support_Calls`: Number of times the user contacted helpdesk (High predictor of frustration).
* `Payment_Delay_Days`: Days late on last invoice.
* `Usage_Frequency`: Platform engagement metric.
* `Contract_Type`: Month-to-month vs. Annual.

## 🏆 Performance Benchmarks

The XGBoost champion model achieved the following baseline metrics during evaluation:
* **Overall Accuracy:** ~92%
* **Recall (Churn Identification):** ~89% *(Optimized to catch maximum at-risk users)*
* **Precision:** ~85%
* **F1-Score:** ~87%

**Key Business Insight:** The model identified that **Support Calls** and **Payment Delay Days** are the highest drivers of customer churn, allowing for targeted marketing interventions.

## 🚦 How to Run the Engine

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/Project-Retention.git](https://github.com/YOUR_USERNAME/Project-Retention.git)
cd Project-Retention
2. Install Dependencies
Bash
pip install pandas numpy scikit-learn xgboost
3. Execute the Notebook
Open Project_Retention.ipynb in Jupyter Notebook, VS Code, or Google Colab, and run the cells sequentially to generate the dataset, train the models, and output the feature importance matrix.

Author: Hemanth Boddupally
