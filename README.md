## Credit Card Customer Segmentation

This project applies **unsupervised machine learning (clustering)** to segment credit card customers into meaningful groups.  
The goal is to provide the marketing team with insights that can guide **targeted strategies** for different types of customers.

---

### 📊 Overview
- **Objective:** Segment customers into groups for targeted marketing.  
- **Techniques Used:** Data cleaning, feature scaling (MinMaxScaler), clustering (Agglomerative & Hierarchical), silhouette evaluation.  
- **Deliverables:** Customer group profiles, visualizations, and actionable marketing recommendations.  

---

### 📂 Dataset
The dataset used is **CC GENERAL.csv**, containing anonymized credit card usage information.  

- **Source:** [Kaggle – Credit Card Dataset for Clustering](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)  
- **Key features include:**  
  - `BALANCE` – Remaining balance in the account.  
  - `PURCHASES` – Total amount spent on purchases.  
  - `CASH_ADVANCE` – Amount borrowed as cash.  
  - `CREDIT_LIMIT` – Credit card limit.  
  - `PAYMENTS` – Amount of payments made.  
  - `TENURE` – Number of months the customer has been with the bank.  

---

### ⚙️ Methodology
1. **Data Cleaning** – handled missing values, removed duplicates, dropped irrelevant columns.  
2. **Exploratory Data Analysis (EDA)** – correlation heatmap, scatter plots, histograms.  
3. **Feature Scaling** – applied MinMaxScaler to normalize feature values.  
4. **Clustering** – tested multiple linkage methods (Ward, Complete, Average).  
5. **Model Evaluation** – used Silhouette Score to find the best model.  
6. **Cluster Profiling** – descriptive statistics + business interpretation for each group.  

---

### 🏆 Results
- **Best Model:** 2 clusters, **Average linkage**, Euclidean metric.  
  - Silhouette Score: **≈ 0.457**  
  - **Cluster 0:** Low/Moderate users (majority group).  
  - **Cluster 1:** High-value customers (smaller group, higher spending and payments).  

- **Alternative Model:** 3 clusters (Average linkage, Silhouette ≈ 0.430).  
  - Cluster 0: Low spenders.  
  - Cluster 1: Moderate spenders.  
  - Cluster 2: High-value customers.  

---

### 🎯 Actionable Marketing Insights
**Cluster 0 (Low/Moderate Users):**  
- Incentivize spending with cashback on everyday purchases.  
- Offer installment plans to encourage bigger purchases.  
- Send targeted campaigns to increase engagement frequency.  

**Cluster 1 (High Users):**  
- Provide premium loyalty programs (travel perks, concierge services).  
- Offer higher credit limits to encourage continued heavy usage.  
- Target with exclusive promotions on luxury items.  

---

### 💻 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/boyejodev/credit-card-segmentation.git
cd credit-card-segmentation
pip install -r requirements.txt
