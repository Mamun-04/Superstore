This project performs exploratory data analysis (EDA) and unsupervised machine learning using KMeans clustering on the popular Superstore dataset. The goal is to segment data points (e.g., transactions or customers) based on sales behavior to uncover patterns in discount usage, profitability, and sales volume.

Sales: Monetary amount of each transaction

Profit: Profit made per transaction

Quantity: Number of items sold

Discount: Discount applied

Postal Code, Product Category, Segment, etc.

Perform EDA to understand the data distribution using descriptive statistics and boxplots.

Use KMeans clustering to group transactions based on their numeric sales-related features.

Visualize and interpret the resulting clusters.


EDA Summary
Initial analysis was done using:

.describe() to check ranges and summary stats.

Boxplots to visualize distribution of:

-Sales (highly skewed with outliers)

-Profit (has negative values)

-Discount

-Quantity

These showed that:

Discounts are usually around 0.2 or 0.0.

Profit and Sales vary widely and have heavy outliers.

Clustering Steps
-Feature Selection
  Chose features: Sales, Profit, Discount, Quantity.

Standardization
-Used StandardScaler to scale features due to different units/ranges.

Elbow Method
-Calculated inertia for K=1 to 10 and plotted the elbow curve to find optimal K.

KMeans Clustering
-Ran KMeans with the selected k, and assigned clusters to each row.

Cluster Analysis
-Aggregated feature values by cluster to interpret differences between clusters.

Visualizations
-Boxplots for EDA

-Elbow Plot to find optimal k

-Pairplot (colored by cluster) to visualize separation in feature space

Key Findings
-Transactions clustered into distinct groups based on how much was sold, discounted, and how profitable they were.
-Some clusters represent high sales, low profit (indicating high discounts), while others had low sales, high profit.
