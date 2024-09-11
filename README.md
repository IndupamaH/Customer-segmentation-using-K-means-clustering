# Customer-segmentation-using-K-means-clustering

# Overview 
The goal is to divide the customer base into distinct groups based on certain characteristics or behaviors in order to better understand the diverse needs and preferences of different customer groups and tailor marketing strategies, product offerings, and services to effectively target each segment. This process is called marketing segmentation.
First we clean and prepare the data for analysis and find the optimal number of clusters using the elbow method. Then, we apply K-means clustering method to perform the cluster analysis. Finally, we use principal component analysis to visualize the clusters.

# Stakeholders
The project like this can be beneficial to banking institutions.
Within the banking institution,

**Marketing Team** can design targeted marketing campaigns and promotions tailored to specific customer segments, enhancing customer acquisition and retention.

**Product Development Team** can understanding different customer needs, they can develop and offer customized financial products and services, such as specialized loan or investment products.

**Customer Service Teams** can provide more personalized service and support, improving customer satisfaction and loyalty.

# KPI 
Key Performance Indicators (KPIs) for a customer segmentation project help measure the effectiveness of the segmentation and its impact on business objectives. Here are some relevant KPIs for such a project:

Segmentation Accuracy:

Cluster Quality Score: Measures how well-defined and distinct the customer segments are. Common metrics include Silhouette Score, Dunn Index, or within-cluster variance.
Homogeneity Score: Measures how similar customers within the same segment are, based on selected features or behaviors.

# Data set 
* The data set is from Kaggle which consists of 6 month sof bank data of its customers. Data Source: https://www.kaggle.com/arjunbhasin2013/ccdata The data set contains features like Bank balance, purchases, payments, and credit limit, etc. 

* **Data Cleaning**
There are some missing values in the minimum payments column and the values were replaced with the mean of the minimum payments values. There were no duplicate entries and the customer_id column was removed before analysis. 

* **Data Pre-Processing and Exploratory Data Analysis**
  By exploring the data set found that
  * Mean of balance is $1500
  * 'Balance_Frequency' for most customers is updated frequently ~1
  * Most of the customers have balance is close to zero.
  * Most of the customers have updated their balance frequently.
  * For 'PURCHASES_FREQUENCY', there are two distinct group of customers. One group of customers have purchase frequency close to zero and other group make frequent payments.
  * PRC_FULL_PAYMENT-shows that most of the customers don't pay the amount in full. a very low number of customers pay the balance in full.
  * For 'ONEOFF_PURCHASES_FREQUENCY' and 'PURCHASES_INSTALLMENT_FREQUENCY' most users don't do one off puchases or installment purchases frequently
  * Very small number of customers pay their balance in full 'PRC_FULL_PAYMENT'~0
  * Credit limit average is around $4500
  * Most customers are ~11 years tenure

# Modeling Approach 


# Conclusion



