# 📦 Warehouse Inventory Optimization using Unsupervised Learning

This project tackles inefficiencies in warehouse storage and inventory management by applying an end-to-end unsupervised machine learning pipeline. Using clustering techniques, the goal is to group SKUs (Stock Keeping Units) with similar behaviors to optimize warehouse layout, reduce operational costs, and improve order fulfillment speed.

---

## 🚀 Project Highlights

- 📊 Applied **feature engineering** to derive actionable metrics like `turnover_rate`, `profit_margin`, and `manufacturing_efficiency`.
- 📉 Performed **dimensionality reduction** using a hybrid approach: **PCA → UMAP → t-SNE**.
- 🤖 Used **KMeans clustering** to segment inventory based on behavioral patterns.
- 📈 Achieved a **silhouette score of 0.5535** — indicating meaningful and well-separated clusters.
- 🔍 Interpreted clusters to support strategic warehouse layout planning.

---

## 🧠 Problem Statement

> Inefficient warehouse space utilization leads to higher storage costs, inventory mismanagement, and delays in order fulfillment.  
> **Objective**: Identify inventory patterns to optimize storage allocation and improve operational performance.

---

## 📁 Dataset Overview

- **Rows**: 100 inventory SKUs
- **Features**: 24 original columns + engineered metrics
- **Includes**: Pricing, stock, lead times, shipping, manufacturing, defects, customer demographics, etc.

---

## 🧪 Methodology

### 1. 📌 Feature Engineering
Derived key metrics:
- `Turnover_rate` = products sold / stock levels
- `Profit_margin` = revenue - cost
- `Manufacturing_efficiency` = volume / lead time
- `Defect_penalty` = defect rate × cost

### 2. 🧹 Preprocessing
- Verified no missing values
- Outlier detection (none found)
- Standardized numerical features using `StandardScaler`

### 3. 📉 Dimensionality Reduction
- **PCA** to reduce noise
- **UMAP** to preserve local/global structure
- **t-SNE** to visualize and prepare for clustering

### 4. 🤖 Clustering with KMeans
- Optimal k = 2 using Elbow + Silhouette methods
- Best Silhouette Score = **0.5535**

### 5. 📊 Cluster Profiling
**Cluster 0**:  
- High stock, bulk production, low profit  
- Lower turnover rate  
- Suited for deep warehouse storage

**Cluster 1**:  
- Fast turnover, high revenue & margin  
- Lower inventory & manufacturing cost  
- Should be placed near dispatch for fast access

---

## 📷 Visual Insights

- ✅ Elbow Method for optimal k  
- ✅ Silhouette Score plot  
- ✅ t-SNE Cluster visualization  
- ✅ Cluster summary tables

---

## 📈 Results

- ✅ Clearly segmented inventory into two behavior-based clusters
- 📦 Recommended storage strategies for each cluster
- 💸 Potential for reduced handling time, better space use, and improved profits

---

## 🛠️ Tech Stack

- Python, NumPy, Pandas, Matplotlib, Seaborn
- Scikit-learn (PCA, KMeans, DBSCAN, t-SNE)
- UMAP-learn
- Google Colab

  ## 🧩 Future Work (Optional Ideas)

- Add a **Streamlit dashboard** to explore clusters interactively
- Include **AutoML** or **HDBSCAN** comparison
- Test with larger, real-world datasets

---

## ✍️ Author

**Sri Harsha Vardhan Chikkala**  
> B.Tech CSE | Big Data Analytics | SRM University - AP  
> 📧 [LinkedIn](https://www.linkedin.com/in/sri-harsha-vardhan-chikkala-7362172b9/) | 🌐 [GitHub](https://github.com/harsha-chikkala)

