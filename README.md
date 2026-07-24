# Week 4 Internship Task
# Customer Segmentation using Unsupervised Learning using K-Means and Hierarchical Clustering:


#  Project Overview

Customer segmentation is one of the most important applications of Machine Learning in the banking and finance industry. Instead of predicting an output variable, this project focuses on discovering hidden patterns among customers based on their credit card usage.

The objective of this project is to group customers into different clusters according to their financial behavior. These customer groups can help banks and financial organizations understand customer spending habits, identify valuable customers, improve marketing campaigns, reduce financial risk, and provide personalized services.

This project implements two popular Unsupervised Machine Learning algorithms:

- K-Means Clustering
- Hierarchical (Agglomerative) Clustering

The performance of both algorithms is analyzed and compared.

#  Objectives of the Project

The main objectives of this project are:

- To understand the concept of Unsupervised Learning.
- To preprocess real-world customer data.
- To clean the dataset and handle missing values.
- To normalize the dataset using feature scaling.
- To determine the optimal number of customer clusters.
- To apply K-Means clustering.
- To evaluate clustering using Elbow Method and Silhouette Score.
- To visualize cluster characteristics using Heatmaps.
- To apply Hierarchical Clustering.
- To compare both clustering techniques.
- To interpret customer groups from a business perspective.


#  Dataset Information

**Dataset Name:** Credit Card Dataset for Clustering

The dataset contains behavioral information of approximately **8950 active credit card customers** over a period of six months.

The dataset consists of **18 numerical features** describing customer purchasing behavior, payment history, balance information, cash advances, and credit utilization.

Some important attributes include:

- BALANCE
- BALANCE_FREQUENCY
- PURCHASES
- ONEOFF_PURCHASES
- INSTALLMENTS_PURCHASES
- CASH_ADVANCE
- PURCHASES_FREQUENCY
- ONEOFF_PURCHASES_FREQUENCY
- PURCHASES_INSTALLMENTS_FREQUENCY
- CASH_ADVANCE_FREQUENCY
- CASH_ADVANCE_TRX
- PURCHASES_TRX
- CREDIT_LIMIT
- PAYMENTS
- MINIMUM_PAYMENTS
- PRC_FULL_PAYMENT
- TENURE

The dataset also contains a customer identifier (CUST_ID), which is removed because it has no impact on clustering.


#  Technologies and Libraries Used

The following technologies were used throughout the project:

### Programming Language

- Python

### Development Environment

- Google Colab

### Python Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy


#  Project Workflow

## Step 1 — Importing Libraries

The required Python libraries were imported to perform data analysis, visualization, preprocessing, clustering, and evaluation.

These libraries include:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- StandardScaler
- KMeans
- AgglomerativeClustering
- Silhouette Score
- Dendrogram


## Step 2 — Loading the Dataset

The dataset was loaded into a Pandas DataFrame.

After loading:

- Dataset shape was checked.
- Column names were inspected.
- Data types were verified.
- Initial rows were displayed using `head()`.

This helped understand the structure of the dataset before preprocessing.


## Step 3 — Data Cleaning

The following preprocessing steps were performed:

### Removing Identifier

The `CUST_ID` column was removed because it only identifies customers and does not provide meaningful information for clustering.

### Handling Missing Values

The dataset contained missing values in a few numerical columns.

Instead of deleting records, missing values were replaced with the mean of their respective columns.

This approach preserves the maximum amount of data while avoiding unnecessary information loss.


## Step 4 — Feature Scaling

Feature scaling was performed using **StandardScaler**.

Scaling is extremely important because clustering algorithms calculate distances between data points.

If one feature has much larger values than others, it dominates the distance calculation and produces poor clusters.

StandardScaler transforms all features so they have approximately:

- Mean = 0
- Standard Deviation = 1

This ensures every feature contributes equally during clustering.


## Step 5 — K-Means Clustering

K-Means clustering was applied for different values of **K** ranging from **2 to 10**.

For each value of K:

- Model was trained.
- Inertia (Within Cluster Sum of Squares) was calculated.
- Results were stored for comparison.


## Step 6 — Elbow Method

The Elbow Method was used to determine the optimal number of clusters.

A graph was plotted between:

- Number of Clusters (K)
- Inertia

The point where the graph begins to bend significantly represents the optimal value of K.

This point indicates that adding more clusters provides only a small improvement.


## Step 7 — Silhouette Score

Silhouette Score was calculated for every value of K.

This score measures how well each customer fits within its assigned cluster.

A higher Silhouette Score indicates:

- Better separation between clusters.
- Better clustering quality.

The Silhouette Score was compared with the Elbow Method to validate the chosen number of clusters.


## Step 8 — Final K-Means Model

After selecting the optimal number of clusters, the final K-Means model was trained.

Cluster labels were assigned to every customer.

A new column named **Cluster** was added to the dataset.


## Step 9 — Cluster Profiling

Each cluster was analyzed separately.

The mean value of every feature was calculated for each cluster.

This helped identify:

- High spending customers
- Low spending customers
- Customers with high balances
- Customers with frequent purchases
- Customers with heavy cash advance usage


## Step 10 — Heatmap Visualization

A heatmap was created using Seaborn.

The heatmap visually compares the average values of every feature across all clusters.

Different colors make it easier to understand the behavior of each customer segment.


## Step 11 — Cluster Interpretation

Each cluster was interpreted from a business perspective.

Examples include:

- High-value customers
- Low-balance customers
- Frequent shoppers
- Cash advance users
- Moderate spending customers

These interpretations help businesses create personalized marketing strategies.


#  Hierarchical Clustering

## Step 12 — Random Sampling

A random sample of 300 customers was selected from the scaled dataset.

Sampling reduces computation time while preserving overall structure.


## Step 13 — Dendrogram

A dendrogram was generated using SciPy.

The dendrogram visually represents how customers merge into clusters.

A horizontal threshold line was added to identify the optimal cut.


## Step 14 — Agglomerative Clustering

Agglomerative Clustering was applied using the same number of clusters selected from K-Means.

Each customer received a hierarchical cluster label.


## Step 15 — Comparing Both Algorithms

A cross-tabulation (`pd.crosstab`) was used to compare cluster assignments.

This comparison shows how similar both algorithms are in grouping customers.


#  Visualizations Included

The notebook contains the following visualizations:

- Dataset Preview
- Elbow Curve
- Silhouette Score Plot
- Cluster Heatmap
- Hierarchical Dendrogram
- Cross Tabulation


#  Results

The project successfully:

- Cleaned and preprocessed the dataset.
- Standardized all numerical features.
- Determined the optimal number of clusters.
- Segmented customers into meaningful groups.
- Compared two clustering algorithms.
- Generated useful visualizations.
- Produced business-friendly customer profiles.


#  Business Applications

The generated customer segments can be used for:

- Personalized Marketing
- Customer Retention
- Credit Risk Analysis
- Customer Loyalty Programs
- Targeted Promotions
- Product Recommendation
- Financial Decision Making


#  Conclusion

This project demonstrates how Unsupervised Machine Learning can discover hidden customer patterns without requiring labeled data.

K-Means proved to be faster and more efficient for larger datasets, while Hierarchical Clustering provided better visualization through the dendrogram.

Both techniques successfully identified meaningful customer segments that can support real-world business decisions.


# 📁 Project Files

- week4_clustering.ipynb
- DataSet(W4).csv
- README.md
- requirements.txt
- documentation


# 👨‍💻 Author

**Name:** Manahil Zahra

**Internship:** AI/ML Internship

**Week:** Week 4

**Project:** Customer Segmentation using K-Means and Hierarchical Clustering
