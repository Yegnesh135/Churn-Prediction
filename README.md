# Churn-Prediction
Customer churn refers to the phenomenon where customers stop doing business with any organization pertaining to various reasons such as dissatisfaction with services, competative offers, technological advancements and personal reasons.Understanding customer churn is crucial for banks as it directly impacts their profitability and sustainability. By identifying the factors contributing to churn, banks can implement strategies to retain their customers and improve overall customer satisfaction. This can involve enhancing customer service, offering competitive products, and leveraging technology to provide a better customer experience.

Machine learning (ML) emerges as a powerful tool in this context, offering a way to predict and mitigate customer churn by analyzing vast datasets, including credit scores and transaction histories. This predictive capability allows banks to identify and retain at-risk customers through targeted interventions, making churn prediction not just a strategic advantage but a necessity in today’s competitive landscape.

The process of churn prediction involves several steps, from data collection and preprocessing to model building and evaluation, employing various ML algorithms like logistic regression, decision trees, neural networks, and more. Each algorithm has its strengths and limitations, but together, they provide a comprehensive approach to understanding and predicting customer behavior. This technological intervention not only helps in retaining customers but also in improving financial planning, enhancing customer satisfaction, and giving banks a competitive edge.

In this project, I worked with a raw dataset from a bank in Botswana, focusing on extensive data cleaning and transformation processes. The key steps included identifying and correcting data types, resolving inconsistencies, handling missing values, removing duplicates, and transforming the data to ensure accuracy and consistency. 

Then out of the total columns, irrelavant columns are dropped. The total number of features came down to 17 (including target) from 25.

The final data comprised of age, Marital Status, Number of Dependents, Occupation, Income, Education Level,	Customer Tenure, Customer Segment, Preferred Communication Channel,	Credit Score,	Credit History, Length	Outstanding Loans, **Churn Flag**, Balance,	NumOfProducts, NumComplaints,	Gender_Male.

From those to be used for model building the categorical data is converted into numerical data using encoding techniques.
Gender : Label Encoding
Marital Status: Label Encoding
Occupation: Frequency Encoding
Education Level: Ordinal Encoding
Customer Segment: Label Encoding
Prefered Communication Channel: One-hot Encoding

The correlation matrix of the data shows a week correlation among features with the target (Churn Flag) as follows:

![image](https://github.com/user-attachments/assets/2ea635e5-62fb-43cb-b1a7-891b05fa48ac)

![Correlation map](https://github.com/user-attachments/assets/0259e5d6-4f29-41f8-885e-805411415281)

After the data cleaning and transformation steps, the dataset was split into training and testing subsets to ensure effective model evaluation. During the analysis of the training data, it became evident that the dataset was imbalanced, which could potentially impact the model's performance by favoring the majority class.

![image](https://github.com/user-attachments/assets/c944c826-b186-4d91-aa6d-372a5605a4fd)

To address this, the Synthetic Minority Over-sampling Technique (SMOTE) was employed. SMOTE is a powerful technique used to balance the dataset by generating synthetic samples for the minority class, thus improving the representation of all classes in the training data. By applying SMOTE, we created a more balanced dataset, which in turn helps the model learn more effectively and reduces bias toward the majority class.

With the dataset balanced, a Logistic Regression model was chosen for training. Logistic Regression is a robust, interpretable algorithm, ideal for classification problems like this one. By training the model on the balanced data, we ensure that it can accurately identify patterns and relationships between features, helping to predict customer churn more effectively.

This approach of handling imbalances, combined with the choice of a well-suited algorithm, lays a solid foundation for achieving improved model performance and delivering actionable insights to reduce churn.

The results of the model are not too fascinating. But should look after the ways to optimize the model. Then use feature importance function to look after the weigths/importance of a column on the target. Thus to make plan of action to act according to minimize the rate of churn.

The classification_report shows up as follows:
  precision    recall  f1-score   support

           0       0.96      0.97      0.97     30464
           1       0.78      0.71      0.74      4228

    accuracy                           0.94     34692
   macro avg       0.87      0.84      0.85     34692
weighted avg       0.94      0.94      0.94     34692

While the initial model results may not have been as impressive as anticipated, this opens up an exciting opportunity for improvement and optimization. By refining the model, we can unlock its true potential. One critical next step is to apply feature importance techniques, which will help us assess the relative influence of each feature on the target variable. Understanding the weight or importance of specific columns can guide us toward making more informed adjustments to the model.

Armed with these insights, we can create a focused plan of action. This may involve prioritizing key features, engineering new ones, or tuning hyperparameters to enhance the model’s performance. The ultimate goal is to minimize the churn rate effectively, based on data-driven decisions.

By embracing this iterative process, we can transform the current outcomes into a more robust, optimized model, driving actionable insights that will lead to meaningful improvements in customer retention strategies.
