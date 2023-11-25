# Project name: Churn Prediction and Segmentation: Machine Learning for Customer Retention.

- Introduction: This project focuses on predicting customer churn and segmenting customers based on their behavior and demographics to develop effective strategies for customer retention. Customer churn, the loss of customers, can have a significant impact on a company's revenue and growth. By understanding the factors that contribute to churn and identifying customer segments, businesses can take proactive steps to retain valuable customers.

- Dataset Description: The dataset used for this project contains the following columns:

	- CustomerID: A unique identifier for each customer.
	- Churn: Whether the customer has left the company's service (1) or not (0).
	- Tenure: The length of time the customer has been with the company (in months).
	- PreferredLoginDevice: The device the customer prefers to use when logging into the service (e.g., Mobile Phone, Computer).
	- CityTier: A classification of the customer's city by certain criteria, such as size or economic activity (Tier 1, Tier 2, etc.).
	- WarehouseToHome: The distance from the warehouse to the customer’s home, possibly in kilometers or miles.
	- PreferredPaymentMode: The customer's preferred method of payment (e.g., Debit Card, UPI, Cash on Delivery).
	- Gender: The customer's gender (e.g., Female, Male).
	- HourSpendOnApp: The average number of hours the customer spends on the company's app.
	- NumberOfDeviceRegistered: The number of devices the customer has registered with the company's service.
	- PreferredOrderCat: The category of products that the customer prefers to order (e.g., Laptop & Accessory, Mobile).
	- SatisfactionScore: A rating of how satisfied the customer is with the company's service, on a scale (e.g., 1-5).
	- MaritalStatus: The marital status of the customer (e.g., Single, Divorced).
	- NumberOfAddress: The number of addresses registered with the company by the customer.
	- Complain: Whether the customer has made a complaint (1) or not (0).
	- OrderAmountHikeFromlastYear: The percentage increase in the customer's order amount compared to the previous year.
	- CouponUsed: The number of coupons used by the customer for purchasing.
	- OrderCount: The number of orders placed by the customer.
	- DaySinceLastOrder: The number of days since the customer's last order.
	- CashbackAmount: The amount of cashback received by the customer.

## Supervised Machine Learning for Churn Prediction
 
- Part I: Exploratory Data Analysis (EDA). During the EDA phase, I will address the following questions and explore the dataset:

	- General Understanding: Are there any missing values? How is the data distributed? What is the overall churn rate in the dataset?
	- Churn Rate and Tenure: How does the churn rate vary with the tenure of the customers? Is there a particular tenure length where churn rate spikes or drops significantly?
	- Demographics and Churn: Are there any noticeable trends in churn when looking at the demographics of the customers, such as gender, marital status, or city tier?
	- Visualize the total number of customers who churned for each distribution of "HourSpendOnApp" and "NumberOfDeviceRegistered.
	- Customer Satisfaction: How does customer satisfaction, as indicated by the satisfaction score, relate to churn? Are less satisfied customers more prone to leaving?
	- Complaints and Churn: Is there a correlation between the number of complaints a customer has made and their likelihood to churn?
	- Product Preferences: Do certain preferred product categories have higher churn rates? For example, are customers who prefer laptops and accessories more loyal than those who prefer mobile phones?
	- Distance Factor: Does the distance from the warehouse to a customer's home have any correlation with churn? Are customers who live farther away more likely to churn?
	- Payment Methods: Is there a preferred payment mode among customers who churn, and how does it compare with those who remain?
	- Financial Behavior: How do the order amount hike from the previous year, coupon usage, and the cashback amount received by customers relate to their likelihood of churning?
	- Service Utilization: Do customers with a higher number of addresses, which may indicate a higher complexity of service use, have different churn rates compared to those with fewer addresses?
	- Create a heatmap to visualize the correlations between numeric columns in the dataset.

- Part II: Minimum Viable Product (MVP): Create a minimum viable product for churn prediction by preprocessing the data.
- Part III: Preprocessing, Feature engineering & complex model: 
	- Data preprocessing involves scaling, encoding, and feature engineering to prepare the data for model training.
	- Model Selection: Experiment with various machine learning models, including RidgeClassifier, RandomForestClassifier, Support Vector Classifier (SVC) and XGBoost Classifier with Hyperparameter Tuning and Evaluation. After rigorous evaluation, I determine that the optimal model for churn prediction is the XGBoost Classifier, which demonstrates superior predictive performance.
- Part IV: Conclusion
	- In summary, our XGBClassifier model performed exceptionally well in predicting customer churn. It achieved high accuracy and ROC AUC scores. While it excelled at identifying non-churned customers, there is room for improvement in correctly identifying churned customers. Overall, the model provides a valuable tool for enhancing customer retention strategies.

## Unsupervised Machine Learning for Customer Segmentation

- Optimal Clustering
Having successfully predicted customer churn, I proceed to segment customers using unsupervised machine learning techniques. Our goal is to identify distinct customer segments based on their behavior, preferences, and demographics.
- Process
Data Transformation: I preprocess the dataset for unsupervised learning, which may include feature scaling and handling categorical variables.
- Clustering: Using techniques such as K-means clustering or hierarchical clustering, I segment customers into distinct groups. In this case, I determine that five optimal clusters provide meaningful insights.
- Interpretation & Insights: Customer segmentation through unsupervised learning has identified five optimal clusters, each with distinct characteristics. Cluster 1 is characterized by customers who predominantly make payments using debit cards, are single or divorced, and have the highest complaint rate, with a significant presence in City Tiers 1 and 3. Cluster 2 consists of single or divorced individuals who exclusively order laptops and accessories and are most commonly associated with City Tier 3; they also have the highest number of addresses. Cluster 3 is marked by a varied payment method preference including debit cards, e-wallets, and cash on delivery, with no complaints and the lowest number of addresses. Cluster 4 customers prefer using debit cards, are married, and all have a complaint rate of 1. Lastly, Cluster 5 includes married customers with no complaints and the highest number of fashion orders

## Conclusion:
- This project encompasses two main phases: churn prediction using supervised machine learning and customer segmentation using unsupervised machine learning. By combining these approaches, businesses can not only predict which customers are likely to churn but also gain a deeper understanding of their customer base, allowing for targeted retention efforts. The optimal model for churn prediction is the XGBoost Classifier, and we identify five distinct customer segments through clustering. These insights can aid in developing strategies to improve customer retention and overall business performance.




