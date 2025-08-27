# Customer Segmentation with K-Means Clustering

## Overview
This project applies **K-Means clustering** to segment customers based on their purchasing behavior. Using a dataset of customer demographics and spending patterns, we identify meaningful groups of customers that can help businesses target their marketing strategies more effectively.

## Steps Performed
1. **Data Preprocessing**
   - Loaded the dataset.
   - Selected relevant features (`Age`, `Annual Income`, `Spending Score`).
   - Scaled the data for clustering.

2. **Choosing Number of Clusters (k)**
   - Used the **Elbow Method** to identify the optimal number of clusters.
   - Selected **k = 4** for segmentation.

3. **Clustering with K-Means**
   - Applied K-Means with `k=4`.
   - Assigned each customer to one of four clusters.

4. **Visualization**
   - Reduced dimensions using **PCA (Principal Component Analysis)**.
   - Plotted the clusters in 2D space for interpretation.

## Results
- Customers are segmented into **four distinct clusters**.
- Each cluster represents a group of customers with similar spending habits and income/age patterns.
- The PCA visualization helps interpret the separation of clusters.

## Files
- `Task1.ipynb` – Jupyter Notebook with the full analysis.
- `README.md` – Project documentation (this file).
- `Mall_customers.csv` – Customer dataset used for clustering.

## Requirements
Install dependencies with:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
