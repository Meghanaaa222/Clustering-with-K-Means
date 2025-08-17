# Customer Segmentation with K-Means Clustering

## Project Overview
This project applies the **K-Means clustering algorithm** to the **Mall Customers dataset** to perform customer segmentation.  
The dataset contains information about customers, and for this project, two features were selected:
- **Annual Income**
- **Spending Score**

The goal is to identify distinct groups of customers based on their income and spending behavior.

## What I Did
1. **Data Loading and Preprocessing**  
   - Loaded the `Mall_Customers.csv` dataset.  
   - Selected **Annual Income** and **Spending Score** as the main features.  
   - Checked for missing values.  
   - Standardized the feature values using `StandardScaler` to ensure fair clustering.  

2. **Finding Optimal K (Number of Clusters)**  
   - Used the **Elbow Method** by plotting Within-Cluster Sum of Squares (WCSS) for K values from 1 to 10.  
   - Determined that **K = 5** gives a good balance for clustering.  

3. **Model Training**  
   - Applied **K-Means clustering** with `n_clusters = 5`.  
   - Assigned each customer to a cluster.  

4. **Visualization**  
   - Plotted the clusters in 2D (Annual Income vs Spending Score).  
   - Highlighted centroids with a yellow star marker.  

5. **Model Evaluation**  
   - Evaluated cluster quality using the **Silhouette Score** (higher values indicate better-defined clusters).  

## What I Got (Results)
- **Optimal Number of Clusters (K):** 5  
- **Cluster Characteristics:**  
  - The algorithm grouped customers into 5 distinct segments based on spending and income levels.  
  - Clear separation between high-income high-spenders, low-income low-spenders, and intermediate groups.  
- **Visualization:** Cluster plot shows meaningful customer groups with well-separated centroids.  

## Conclusion
K-Means clustering successfully segmented customers into 5 groups.  
This type of analysis can help businesses in **targeted marketing**, **customer relationship management**, and **product recommendations**.  
However, results may vary with different features or scaling methods, and advanced clustering methods (like DBSCAN or hierarchical clustering) could be explored for more complex datasets.

## How to Use
- Place the `Mall_Customers.csv` file in the same directory as the notebook.  
- Open the notebook in **Jupyter Notebook** or **JupyterLab**.  
- Run all cells in order.  
- The notebook will:  
  - Show the Elbow Method plot to determine optimal K.  
  - Train the K-Means model with K = 5.  
  - Visualize clusters with centroids.  
  - Print cluster assignments for each customer.  
