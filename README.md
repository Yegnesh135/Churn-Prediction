# Churn-Prediction
Customer churn refers to the phenomenon where customers stop doing business with any organization pertaining to various reasons such as dissatisfaction with services, competative offers, technological advancements and personal reasons.Understanding customer churn is crucial for banks as it directly impacts their profitability and sustainability. By identifying the factors contributing to churn, banks can implement strategies to retain their customers and improve overall customer satisfaction. This can involve enhancing customer service, offering competitive products, and leveraging technology to provide a better customer experience.

In this project I choose a very raw dataset of a bank from Botswana, where a series of data cleaning and transforming steps such as identifying datatypes, checking for inconsistencies, handling missing values, correcting inconsistent data, removing duplicates, transforming data and validating it were performed. To be precise the data type of the Date of Birth is object. This is then converted into datatime datatype. Then the column is used to calculate the age.  

Then out of the total columns, irrelavant columns are dropped, and from those to be used for model building the categorical data is converted into numerical data using encoding techniques. Here I used one-hot encoding, label encoding, ordinal encoding and frequency encoding as per the need of the feature.

Then the data is split into train and test data sets. The train dataset is identified as imbalanced one and SMOTE technique is used to balance the dataset. And then Logistic regression is used to train the model. 

The results of the model are not too fascinating. But should look after the ways to optimize the model. Then use feature importance function to look after the weigths/importance of a column on the target. Thus to make plan of action to act according to minimize the rate of churn.
