# eComerce Customer Segmentation

<img width="350" alt="segmentation " src="https://github.com/Weilin-Liao1/sql_projects/assets/82377749/a083eae1-de52-4878-a2fa-ae2e82e8d57b">

Image source: <a href="https://shorturl.at/mzPR5"> mybizmarketer </a>


## Introduction and Tools 

**Customer Segmentation**

Customer segmentation is the process of dividing customers into several homogeneous clusters based on various attributes. Therefore customers in the same group are similar in demographic or behavioral characteristics, but customers in different sets are distinct. It is used as a differentiation marketing tool enabling firms to understand their customers and develop differentiated strategies based on their characteristics.

Customer segmentation in marketing can be used in the following areas:

- **Deepen the understanding of customers** to support the discovery of new marketing opportunities.
- **Design and develop new products/services and product packages specific to each market segment** rather than the mass market.
- **Creation of customized product offering strategies to existing customers** according to each segment's identified needs.
- **Provide tailored rewards and incentives.**
- **Choose appropriate advertisements and exchange information and channels.**
- Select differentiated customer service based on the importance of each segment.
- **Allocate resources more efficiently** based on the potential return from each segment.
- **Prioritize marketing plans** aimed at retaining customers and development according to each segment's importance. 

**RFM analysis:**

RFM analysis is a popular approach to understand customer buying behavior. 
It involves three database marketing metrics: Recency (R), frequency (F), and monetary value (M) : 
 
 - **Recency:** The time when the customer recently purchased the product
 - **Frequency:** The frequency of customer purchases
 - **Monetary:** Value of the purchase

RFM analysis can identify the best customers with the highest scores in the relevant metrics, and these customers usually tend to make more purchases. It can also identify other purchase patterns and corresponding customer types of interest, such as large customers that are not purchasing frequently or customers who purchase a small number of times but purchase frequently. These customers may also have sales prospects, depending on the market and the specific promotion. RFM analysis is treated as one of the "predictive model" used in database marketing. 


**Cluster Analysis**

Segmentation is the process of grouping customers based on similarity, while clustering is the process of finding similarities among customers to group and segment them.

Clustering uses machine learning and algorithms to identify how different types of data are related and create new segments based on these relationships. Clustering discovers relationships between data points so that they can be segmented. Its purpose is only to divide the subject into several homogeneous groups. 

Several algorithms are available for clustering, and they are roughly divided into hierarchical and nonhierarchical clustering techniques. Hierarchical clustering is classified into two categories: agglomerative and divisive method. Further, non-hierarchical clustering contains three submethods: K-means clustering, probabilistic clustering, and self-organizing maps. 

The choice of these methods is usually subjective, and not all marketers consider one to be the optimal set of options. The choice of method usually depends on the question – are the results useful? This approach will be further discussed as the K-means is seen as the most popular clustering method among data miners. 

**K-means Clustering**

![image](https://user-images.githubusercontent.com/82377749/120203694-49f1dd00-c228-11eb-9531-00c7ba2ee9b8.png)

Image source: <a href="https://rpubs.com/cyobero/k-means"> rpubs.com </a>

K-means clustering starts by randomly assigning n customers to K clusters and gradually improves the partition by changing the cluster membership of each customer. 

In more detail, given a user-specified number of clusters k, the algorithm starts by randomly selecting k points among the n customers that become the centre of the initial cluster. According to the Euclidean distance, each remaining customer is assigned to one of the k cluster centres. After grouping all customers into k clusters, a new cluster "centre" will be calculated, usually as the average value of each cluster variable in each set. And then, based on the distance from these new cluster centres, redistribute each topic. We will stop the iteration when no more redistribution occurs.

## eCommerce Customer Segmentation Projects

As mentioned above, based on the RFM metrics, we can group customers and make marketing suggestions. For example, we can offer promotions to re-engage customers who have not recently purchased items. We can further prioritize our promotional strategy by focusing on customers who shop frequently and consume at least the average monetary value.

However, the traditional RFM method requires ranking customers manually according to the RFM scores. More complex and less manual processes: k-means clustering analysis can be implemented, so that customer groups have more similar characteristics.

Therefore, I will create two sub-projects, one only applying the traditional RFM analysis and another one implementing the RFM analysis and then applying the k-means clustering. In turn, we can compare the results of these two approaches. 

- **Project 1.  eCommerce Customer Segmentation (RFM Analysis)**
- **Project 2.  eCommerce Customer Segmentation (RFM Analysis + K-Means Clustering)**


## Data and references

**Data:**

It is often challenging to find publicly available e-commerce datasets as they tend to be proprietary. However, the <a href="https://archive.ics.uci.edu/ml/datasets/online+retail "> UCI Machine Learning Repository</a> offers this dataset, which includes actual transactions spanning 1 year. The dataset is maintained on their website under the title 'Online Retail.' This multinational dataset contains all the transactions that took place between 2010 and 2011 for non-store online retail businesses registered in the UK. The company primarily deals in unique all-occasion gifts, and many of its clients are wholesalers

**Reference:** 

- Blattberg, R. C., Kim, B.-D., &amp; Neslin, S. A. (2008). Database Marketing Analyzing and Managing Customers. Springer New York. 
- Correia, J. (2020, June 2). How RFM Analysis Boosts Sales: Blast Analytics &amp; Marketing. Blast Analytics. https://www.blastanalytics.com/blog/rfm-analysis-boosts-sales. 
- RFM Segmentation: RFM Analysis, Model, Marketing &amp; Software. Optimove. (2020, May 25). https://www.optimove.com/resources/learning-center/rfm-segmentation. 


**Python Version:** 3.8.3

**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, squarify, datetime

**Modules:** StandardScaler, KMeans, pyplot, date



