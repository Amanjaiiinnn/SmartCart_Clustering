# SmartCart_Clustering

## SmartCart Customer Segmentation Analysis

This project performs customer personality analysis and segmentation for 'SmartCart' retail data to help the business better understand its customers and optimize marketing strategies.

## Project Overview
The goal of this project is to group customers based on their purchasing behavior, demographics, and engagement levels using unsupervised machine learning techniques.

## Dataset
The dataset `smartcart_customers.csv` contains information on 2,240 customers across 22 initial features, including:
- **Demographics:** Age, Education, Marital Status, Income, and Household size.
- **Products:** Amount spent on Wine, Fruits, Meat, Fish, Sweets, and Gold.
- **Promotion/Place:** Number of deals used and purchases made via Web, Catalog, or Store.

## Key Workflow
1. **Data Cleaning:** 
   - Handled missing values in `Income` using the median.
   - Removed outliers in `Age` and `Income` for better cluster stability.
2. **Feature Engineering:** 
   - Created `Age`, `Total_Spending`, `Total_Children`, and `Customer_Tenure_Days`.
   - Simplified `Education` and `Marital_Status` (Living_With) categories.
3. **Preprocessing:** 
   - One-Hot Encoding for categorical variables.
   - Standard Scaling for numeric features.
4. **Dimensionality Reduction:** 
   - Applied **PCA (Principal Component Analysis)** to reduce features to 3 components for better visualization and noise reduction.
5. **Clustering:**
   - Used the **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters (k=4).
   - Implemented **Agglomerative Clustering** with 'ward' linkage.

## Insights from Clusters
- **Cluster 0 & 2:** Lower income, higher number of children, and lower total spending. Likely sensitive to deals.
- **Cluster 1 & 3:** High income, fewer children, and significantly higher spending across all categories. These represent the 'Elite' or 'High-Value' segments.

## Technologies Used
- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn (PCA, StandardScaler, AgglomerativeClustering)
- Kneed (KneeLocator)
