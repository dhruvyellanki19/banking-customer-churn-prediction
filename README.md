# **Customer Churn Prediction and Retention Strategy in Banking**  

## **Overview**  
Customer churn is a big challenge for banks. Losing customers not only affects revenue but also increases costs to attract new ones. Retaining existing customers is much cheaper than acquiring new ones, making it important to predict churn and take action early.  
This project applies machine learning to build a predictive model for identifying customers likely to leave based on key factors such as age, balance, credit score, tenure, number of products used, and active membership status. By analyzing customer behaviors and financial attributes, banks can take proactive measures to enhance engagement and minimize churn."

<p align="center">
  <img src="https://github.com/dhruvyellanki19/project_images/blob/d1d70cea0d3640f095884f7d51545d3c0d5da85d/churn_prediction_pic.jpeg" width="500"/>
</p>

---

## **Problem Statement**  
Many banks struggle to understand why customers leave. Traditional retention strategies rely on historical data but lack predictive insights, making it difficult to act before churn happens. This project bridges that gap by leveraging machine learning to identify at-risk customers early, analyze key churn factors, and recommend targeted retention strategies.  

Therefore, this project builds a predictive model to help banks:  
- Identify customers at risk of churning before they leave.  
- Understand key factors influencing churn like balance, membership status, and product usage.  
- Improve customer retention by providing personalized offers and engagement strategies.  

---

## **Dataset and Features**  
- **Dataset:** Bank customer churn dataset  
- **Size:** 10,000 customer records  
- **Key Features:**  
  - **Demographic Information:** Age, Gender, Geography  
  - **Financial Information:** Credit Score, Account Balance, Estimated Salary  
  - **Banking Behavior:** Tenure, Number of Products Used, Active Membership, Credit Card Ownership  
  - **Target Variable:** Churn (1 = Churned, 0 = Retained)  

---

## **Exploratory Data Analysis (EDA)**  
Before building models, we explored the data to find important trends:  
- **Churn Rate:** Around 20.37% of customers left, showing an imbalance in the dataset.  
- **Age and Churn**: Older customers showed a higher tendency to churn, possibly due to shifting financial needs or dissatisfaction with digital banking services.  
- **Balance and Churn:** Customers with zero balance had a higher churn rate.  
- **Active Membership:** Customers without an active membership were much more likely to churn.  
- **Number of Products Used**: Customers using only one banking product had a higher churn risk, while those with multiple products showed stronger loyalty, emphasizing the importance of cross-selling financial services.  

### **Feature Engineering**  
To improve model accuracy, we created additional features:  
- **Zero Balance Indicator:** A new binary feature identifying customers with zero account balance, which strongly correlates with churn likelihood..  
- **Interaction Features:** Captures relationships between credit score, tenure, and balance.  
- **Categorical Encoding:** Converted categorical variables into numerical representations for machine learning compatibility..  

---

## **Model Development and Evaluation**  
We trained multiple machine learning models and optimized them to get the best performance:  

| **Model**            | **Accuracy** | **AUC Score** |  
|----------------------|-------------|--------------|  
| Random Forest       | **86.50%**   | **0.86**      |  
| Support Vector Machine (SVM) | 85.60%  | 0.83         |  
| Logistic Regression | 81.20%       | 0.78         |  
| Decision Tree       | 78.15%       | 0.67         |  

### **Hyperparameter Tuning**  
To improve performance, we used GridSearchCV and RandomizedSearchCV to optimize model parameters:  
- **Random Forest:** Tuned the number of trees, depth, and feature selection.  
- **SVM:** Adjusted the kernel function and regularization.  
- **Logistic Regression:** Optimized regularization strength and solver.  

Random Forest achieved the highest accuracy (86.45%) and AUC score (0.86), making it the most reliable model for predicting customer churn. It outperformed other models due to its ability to handle non-linear relationships and feature interactions, which are crucial in customer retention analysis. 

### **Feature Importance Analysis**  
The **Random Forest model** showed that the following factors had the biggest impact on customer churn:  


| **Feature**            | **Importance (%)** | **Why It Matters** |  
|------------------------|------------------|----------------------|  
| **Account Balance**    | **29.6%**        | Customers with very high or very low balances may be disengaged from banking services. |  
| **Credit Score**       | **25.3%**        | Poor credit scores may indicate financial instability, increasing churn risk. |  
| **Active Membership**  | **18.2%**        | Inactive customers are more likely to leave if not engaged proactively. |  
| **Number of Products** | **15.4%**        | Customers using only one product are at higher risk, highlighting cross-sell opportunities. |  
| **Tenure**            | **8.1%**         | Long-term customers are generally more loyal, but disengagement can lead to churn. |"_  


---

## **Key Findings and Business Recommendations**  

- **Identify High-Risk Customers Early:** The model allows early detection of customers likely to leave, enabling proactive intervention.
- **Enhance Customer Engagement:** Customers with low product usage and inactive memberships should be targeted with personalized banking solutions.
- **Offer Personalized Retention Strategies:** Banks can provide loyalty programs, exclusive discounts, and financial incentives to keep customers engaged.
- **Improve Banking Experience:** Investing in better customer service, rewards programs, and simplified account management can reduce churn.

---

## **Future Scope**  

🔹 **Real-Time Monitoring and Alerts:** Integrate real-time data for instant churn detection and intervention.  
🔹 **Periodic Model Updates:** Regularly retrain the model with new customer data to keep it accurate.  
🔹 **Feature Expansion:** Add customer spending habits, service feedback, and transaction frequency to improve predictions.  
🔹 **Advanced AI Techniques:** Use deep learning models to increase accuracy.  

---

## **Conclusion**  

This project successfully developed a customer churn prediction model, providing banks with a powerful tool to minimize customer attrition and improve engagement strategies.  

- **Random Forest** emerged as the most effective model, achieving 86.50% accuracy.  
- By analyzing account balance, credit score, product usage, and active membership, banks can now identify customers at risk of leaving before they churn.  
- With real-time monitoring and continuous improvements, this model can be integrated into banking platforms to provide better retention strategies and an enhanced customer experience.  

This project serves as a foundation for data-driven decision-making, enabling banks to take early action, improve customer satisfaction, and drive long-term profitability.  
