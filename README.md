# Customer-segmentation-using-K-means-clustering

# Overview 
The goal of this project is to divide the customer base into distinct groups based on certain characteristics or behaviors in order to better understand the diverse needs and preferences of different customer groups and tailor marketing strategies, product offerings, and services to effectively target each segment. This process is called marketing segmentation.
First we clean and prepare the data for analysis and find the optimal number of clusters using the elbow method. Then, we apply K-means clustering method to perform the cluster analysis. Finally, we use principal component analysis to visualize the clusters.

# Stakeholders
The project like this can be beneficial to banking institutions.
Within the banking institution,

**Marketing Team** can design targeted marketing campaigns and promotions tailored to specific customer segments, enhancing customer acquisition and retention.

**Product Development Team** can understanding different customer needs, they can develop and offer customized financial products and services, such as specialized loan or investment products.

**Customer Service Teams** can provide more personalized service and support, improving customer satisfaction and loyalty.

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
    ![KDE purchace frequency](https://github.com/user-attachments/assets/aef0d4fd-4ceb-48d3-8e71-e0455dfc2bcb)
  * PRC_FULL_PAYMENT-shows that most of the customers don't pay the amount in full. a very low number of customers pay the balance in full.
  * For 'ONEOFF_PURCHASES_FREQUENCY' and 'PURCHASES_INSTALLMENT_FREQUENCY' most users don't do one off puchases or installment purchases frequently
  * Very small number of customers pay their balance in full 'PRC_FULL_PAYMENT'~0
  * Credit limit average is around $4500
  * Most customers are ~11 years tenure
  * The correlation heatmap between the featurs shows that # Purchases have high correlation with oneoff_purchases(0.92), installments_purchases(0.68), and purchases_TRX(0.69).
    ![heatmap](https://github.com/user-attachments/assets/91a6832f-d4c8-4188-a243-39c8aeb96f1a)
# Modeling Approach 
## Elbow Method
Here we apply K-means clustering method to find the clusters. To find the optimal number of clusters k, the elbow method is used. 
The elbow method is a heuristic method of interpretation and validation of consistency within cluster analysis designed to help find the appropriate number of clusters in a dataset.
If the line chart looks like an arm, then the "elbow" on the arm is the value of k that is the best.
The figure below shows the k value as 5 for 7 features of the data set.

![elbow method](https://github.com/user-attachments/assets/1c832df7-3fb3-4c0b-a210-cc3701551e33)

After experimenting with different set of features and the elbow method settled on using 4 clusters. 
After applying the K means clustering method we get the cluster centers. By looking at the values at each column of the cluster centers, we can identify characteristics of each cluster. 

* **Cluster 1(Transactors)**: Those are customers who pay least amount of intrerest charges and careful with their money, Cluster with lowest balance ($104) and cash advance ($303), Percentage of full payment = 23%

* **Cluster 2 (revolvers)**: who use credit card as a loan (most lucrative sector): highest balance ($5000) and cash advance (~$5000), low purchase frequency, high cash advance frequency (0.5), high cash advance transactions (16) and low percentage of full payment (3%)

* **Cluster 3 (VIP/Prime)**: high credit limit $16K and highest percentage of full payment, target for increase credit limit and increase spending habits

* **Cluster 4 (low tenure)**: these are customers with low tenure (7 years), low balance

## Principal Component Analysis(PCA) to visualize the results
We can use PCA to visualize the 4 clusters.

![PCA](https://github.com/user-attachments/assets/4cb8f0d2-484b-450f-b492-f45864078aea)





