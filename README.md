Practical 9 -- Customer Segmentation Using Clustering
Aim
To develop machine learning models using K-Means Clustering and
Hierarchical Clustering to identify customer or data segments and
compare the performance of both clustering techniques.
Dataset Used
The notebook loads the Wholesale Customers dataset from:

Wholesale customers data - Wholesale customers data.csv

The dataset contains 440 rows and 8 columns:
- Channel
- Region
- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicassen
Important note: The aim text in the notebook describes a shopping
mall customer-segmentation example using Age, Annual Income and Spending
Score. However, the code actually loads and analyzes the Wholesale
Customers dataset with the eight columns listed above. This README
describes the dataset and implementation used by the notebook.
Algorithms and Techniques
- K-Means Clustering: Partitions the data into a selected number
  of clusters.
- Hierarchical Clustering: Builds a hierarchy of clusters and
  visualizes it using dendrograms.
- StandardScaler: Standardizes the input features before
  clustering.
- Elbow Method (WCSS): Examines within-cluster sum of squares for
  different cluster counts.
- Silhouette Score: Evaluates how well-separated the clusters are.
- PCA: Reduces the standardized data to two components for
  visualization.
Workflow
1. Import the required Python libraries.
2. Load the Wholesale Customers CSV file into a Pandas DataFrame.
3. Inspect the first rows, dataset shape, data types and summary
   statistics.
4. Check for duplicate rows and missing values.
5. Perform exploratory data analysis using histograms, KDE plots,
   boxplots and a correlation heatmap.
6. Detect potential outliers using the IQR method.
7. Standardize the dataset using StandardScaler.
8. Apply the Elbow Method for cluster counts from 1 to 10.
9. Calculate Silhouette Scores for K-Means models with 2 to 10
   clusters.
10. Select the cluster count with the highest Silhouette Score.
11. Train the K-Means model and examine the resulting cluster sizes.
12. Perform Hierarchical Clustering using Ward linkage and display full
    and truncated dendrograms.
13. Apply PCA to reduce the standardized data to two components and
    visualize the K-Means clusters.
14. Fit Agglomerative Hierarchical Clustering using the selected number
    of clusters.
15. Compare K-Means and Hierarchical Clustering using Silhouette Scores
    and cluster counts.
16. Compare cluster sizes and inspect the mean feature values for each
    K-Means cluster.
Results Recorded in the Notebook
- Dataset size: 440 records × 8 columns.
- No missing values were reported.
- Duplicate-row count: 0.
- The maximum Silhouette Score among the tested K-Means cluster counts
  was 0.3742, obtained with 2 clusters.
- K-Means cluster sizes: 140 and 300.
- Hierarchical Clustering Silhouette Score: 0.3680, with 2
  clusters.
- K-Means Silhouette Score: 0.3742, with 2 clusters.
- The first two PCA components explain approximately 61.1% of the
  variance.
Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
Files
- Lab_9(ML).ipynb -- Jupyter Notebook containing the practical
  implementation.
- Wholesale customers data - Wholesale customers data.csv -- Dataset
  file required by the notebook.
- README.md -- Project description and instructions.
How to Run
1. Download or clone this repository.
2. Install Python and Jupyter Notebook, or open the notebook in Google
   Colab.
3. Install the required libraries:
   pip install pandas numpy matplotlib seaborn scikit-learn scipy
4. Keep the CSV file in the same working folder as the notebook, using
   the exact filename:
   Wholesale customers data - Wholesale customers data.csv
5. Open Lab_9(ML).ipynb and run the cells from top to bottom.
Conclusion
The notebook applies K-Means and Hierarchical Clustering to the
Wholesale Customers dataset after standardizing the features. It uses
the Elbow Method and Silhouette Score to select and evaluate clusters,
dendrograms to inspect hierarchical grouping, and PCA to visualize the
K-Means segments. In the recorded comparison, K-Means achieved a
Silhouette Score of approximately 0.3742, slightly higher than the
Hierarchical Clustering score of approximately 0.3680.
