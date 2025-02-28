# **Customer Churn Prediction and Retention Strategy in Banking**  

## **Overview**  
Customer churn is a big challenge for banks. Losing customers not only affects revenue but also increases costs to attract new ones. Retaining existing customers is much cheaper than acquiring new ones, making it important to predict churn and take action early.  

This project uses machine learning to predict customer churn based on age, balance, credit score, tenure, number of products used, and active membership status. By identifying customers who are likely to leave, banks can **improve engagement, offer better services, and reduce churn**.  

---

## **Problem Statement**  
Many banks struggle to understand why customers leave. Traditional methods rely on past data but **lack predictive power** to take early action.  

This project builds a predictive model to help banks:  
- Identify customers at risk of churning before they leave.  
- Understand key factors influencing churn like balance, membership status, and product usage.  
- Improve customer retention by providing personalized offers and engagement strategies.  

<p align="center">
  <img src="https://github.com/dhruvyellanki19/project_images/blob/d1d70cea0d3640f095884f7d51545d3c0d5da85d/churn_prediction_pic.jpeg" width="500"/>
</p>

---

## **Dataset & Features**  
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
- **Age & Churn:** Older customers were more likely to leave.  
- **Balance & Churn:** Customers with zero balance had a higher churn rate.  
- **Active Membership:** Customers without an active membership were much more likely to churn.  
- **Number of Products Used:** Customers using only one product had a higher risk of leaving, while those using more banking products were more likely to stay.  

### **Feature Engineering**  
To improve model accuracy, we created additional features:  
- **Zero Balance Indicator:** Identifies customers with zero account balance.  
- **Interaction Features:** Captures relationships between credit score, tenure, and balance.  
- **Encoded Categorical Variables:** Converts gender, geography, and credit card ownership into numerical values.  

---

## **Model Development & Evaluation**  
We trained multiple machine learning models and optimized them to get the best performance:  

| **Model**            | **Accuracy** | **AUC Score** |  
|----------------------|-------------|--------------|  
| Random Forest       | **86.45%**   | **0.86**      |  
| Support Vector Machine (SVM) | 85.60%  | 0.83         |  
| Logistic Regression | 81.20%       | 0.78         |  
| Decision Tree       | 78.15%       | 0.67         |  

### **Hyperparameter Tuning**  
To improve performance, we used GridSearchCV and RandomizedSearchCV to optimize model parameters:  
- **Random Forest:** Tuned the number of trees, depth, and feature selection.  
- **SVM:** Adjusted the kernel function and regularization.  
- **Logistic Regression:** Optimized regularization strength and solver.  

**Random Forest** performed the best with **86.45% accuracy and an AUC score of 0.86**, making it the most effective model.  

### **Feature Importance Analysis**  
The **Random Forest model** showed that the following factors had the biggest impact on customer churn:  

| Feature | Importance (%) |
|---------|--------------|
| Account Balance | **29.6%** |
| Credit Score | **25.3%** |
| Active Membership | **18.2%** |
| Number of Products Used | **15.4%** |
| Tenure | **8.1%** |

---

## **Key Findings & Business Recommendations**  

🔹 **Identify high-risk customers early:** The model can flag customers before they leave, allowing banks to take action.  
🔹 **Improve customer engagement:** Customers with low product usage and inactive memberships should be offered better banking solutions.  
🔹 **Personalized retention strategies:** Banks can offer loyalty programs, discounts, and exclusive benefits to at-risk customers.  
🔹 **Enhance banking experience:** Better customer service, rewards programs, and simpler account features can help reduce churn.  

---

## **Future Scope**  

🔹 **Real-Time Monitoring & Alerts:** Integrate real-time data for instant churn detection and intervention.  
🔹 **Periodic Model Updates:** Regularly retrain the model with new customer data to keep it accurate.  
🔹 **Feature Expansion:** Add customer spending habits, service feedback, and transaction frequency to improve predictions.  
🔹 **Advanced AI Techniques:** Use deep learning models to increase accuracy.  

---

## **Conclusion**  

This project successfully built a customer churn prediction model that helps banks reduce attrition and improve customer retention.  
The Random Forest model was the best performer, achieving 86.45% accuracy. By analyzing balance, credit score, product usage, and active membership, banks can now identify customers at risk of churning before they leave.  
With ongoing improvements, this model can be integrated into banking systems to provide real-time predictions, better retention strategies, and increased customer satisfaction.  
