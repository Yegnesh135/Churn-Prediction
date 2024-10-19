![image](https://github.com/user-attachments/assets/9549ec90-b14a-45de-b47d-b9fae2e56b50)# Churn-Prediction
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

Then the data is split into train and test data sets. The train dataset is identified as imbalanced one and SMOTE technique is used to balance the dataset. And then Logistic regression is used to train the model. 

The results of the model are not too fascinating. But should look after the ways to optimize the model. Then use feature importance function to look after the weigths/importance of a column on the target. Thus to make plan of action to act according to minimize the rate of churn.

![Correlation map](https://github.com/user-attachments/assets/0259e5d6-4f29-41f8-885e-805411415281)

