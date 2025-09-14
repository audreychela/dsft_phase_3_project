# 📌 Churn Prediction Project  

## 1.) Overview  
This project aims to build a machine learning model to predict **customer churn** in a telecom company. Customer churn occurs when subscribers stop using a service, leading to revenue loss. By predicting churn early, the company can take proactive actions such as improving customer service, offering targeted promotions, or adjusting pricing strategies.  

---

## 2.) Business and Data Understanding  
### Business Problem  
Customer retention is often more cost-effective than acquiring new customers. High churn rates directly affect profitability. This project addresses the following key question:  
👉 *Which customers are most likely to churn, and what are the main factors driving this behavior?*  

### Dataset Choice  
The dataset I  used is a **SyriaTel Customer Churn** containing both **customer demographics** and **service usage data**.  
- Features include: account length, number of customer service calls, international plan, voice mail plan, total call minutes, and total calls.  
- Target variable: `churn' (1 = customer churned, 0 = customer retained).  

This dataset helps to capture both **behavioral patterns** (usage, calls, minutes) and **service experience** (customer service calls, plan types) that influence churn. 

## 3). Exploratory Data Analysis (EDA)  
To better understand the dataset, I performed:  

- **Univariate Analysis**:  
  Examined distributions of single variables such as account length, customer service calls, total day minutes, and churn rate. This helped reveal class imbalance (fewer churners than non-churners).  

- **Bivariate Analysis**:  
  Explored relationships between features and churn. For example, customers with more than 3 customer service calls had significantly higher churn rates.  

- **Multivariate Analysis**:  
  Scatterplots and correlation heatmaps were used to study interactions between multiple variables. This revealed how service plans and call usage combined with customer service interactions influenced churn.  

These insights guided **feature engineering** (for example, merging total call minutes, creating usage bins) and improved model performance.  


---

## 4). Modeling  
Several machine learning models were built and compared:  
- **Logistic Regression** – baseline model for interpretability.  
- **Decision Tree** – to capture non-linear relationships.  
- **Random Forest** – ensemble method to improve performance.  
- **XGBoost** – gradient boosting model for high accuracy.  

To handle **class imbalance** (fewer churners than non-churners), I  applied **SMOTE (Synthetic Minority Oversampling Technique)** to balance the training data.  

---

## 5.) Evaluation  
Models were evaluated using:  
- **Accuracy** – overall correct predictions.  
- **Precision & Recall** – especially recall to minimize false negatives (missing actual churners).  
- **F1-score** – balance between precision and recall.  
- **Confusion Matrix** – to visualize performance on positives and negatives.  

Feature importance was also analyzed to understand which factors influence churn the most. Key drivers identified include **total call minutes**, **customer service calls**, and **account length**.  

---

## 6). Conclusion  
- **Random Forest and XGBoost** performed the best after applying SMOTE, balancing precision and recall.  
- **Customer service calls** and **call usage patterns** are the strongest predictors of churn.  
- Business can reduce churn by focusing on **improving customer service experiences** and monitoring customers with unusually high call minutes or frequent complaints.  

✅ This project demonstrates how machine learning can be used to predict churn and guide **data-driven retention strategies**.  
