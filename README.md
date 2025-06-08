# K-Means Clustering on Mall Customers Dataset

## Project Overview
Welcome to the **K-Means Clustering on Mall Customers Dataset** project! This project applies K-Means clustering to segment mall customers based on their annual income and spending score, using the `Mall_Customers.csv` dataset. Designed by a data analyst, this project demonstrates a complete clustering pipeline, including data visualization, optimal cluster selection, and evaluation. The goal is to identify distinct customer groups for targeted marketing strategies.

### Key Objectives
- **Data Visualization**: Visualize the dataset in 2D using PCA for better understanding.
- **K-Means Clustering**: Apply K-Means to assign customers to clusters.
- **Optimal K Selection**: Use the Elbow Method to determine the best number of clusters.
- **Cluster Visualization**: Display clusters with color-coding for interpretability.
- **Evaluation**: Assess clustering quality using the silhouette score.

## Dataset
The `Mall_Customers.csv` dataset contains 200 entries with the following features:
- **CustomerID**: Unique identifier (not used in clustering)
- **Gender**: Customer gender (not used in this analysis)
- **Age**: Customer age (not used in this analysis)
- **Annual Income (k$)**: Annual income in thousands of dollars (used for clustering)
- **Spending Score (1-100)**: Score assigned based on spending behavior (used for clustering)

### Dataset Features for Clustering
This project focuses on two features:
- `Annual Income (k$)`: Represents the financial capacity of customers.
- `Spending Score (1-100)`: Reflects spending behavior, with higher scores indicating higher spending.

## Technologies Used
- **Python 3.8+**: Core programming language
- **Pandas**: Data loading and manipulation
- **NumPy**: Numerical computations
- **Scikit-learn**: K-Means clustering, PCA, scaling, and silhouette score
- **Matplotlib/Seaborn**: Visualization of clusters and evaluation plots
- **Jupyter Notebook** (optional): For interactive development

## Prerequisites
Before running the project, ensure you have the following:
- Python 3.8 or higher
- Required libraries:
  ```bash
  pip install pandas numpy scikit-learn matplotlib seaborn
  ```
- The `Mall_Customers.csv` dataset in the project directory

## Installation and Usage
Follow these steps to set up and run the project on your local machine:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/kmeans-mall-customers-clustering.git
   cd kmeans-mall-customers-clustering
   ```

2. **Set Up a Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   Alternatively, install the required libraries directly:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```

4. **Prepare the Dataset**:
   - Ensure `Mall_Customers.csv` is in the project directory.
   - The script handles data preprocessing automatically.

5. **Run the Script**:
   Execute the main script to perform clustering, visualize results, and evaluate performance:
   ```bash
   python kmeans_mall_customers_clustering.py
   ```
   Alternatively, use a Jupyter Notebook by opening `kmeans_mall_customers_clustering.ipynb` (if provided).

6. **View Outputs**:
   - **Visualizations**: PCA plot, Elbow Method plot, cluster scatter plots (original features and PCA), and silhouette score plot.
   - **Console Output**: Silhouette scores for different `K` values.

## Project Workflow
1. **Data Loading and Visualization**:
   - Load the dataset using Pandas.
   - Select `Annual Income (k$)` and `Spending Score (1-100)` for clustering.
   - Scale features using `StandardScaler`.
   - Apply PCA to reduce to 2D and visualize the data distribution.

2. **K-Means Clustering**:
   - Perform initial clustering with `K=3`.
   - Assign cluster labels to each customer.

3. **Optimal K Selection**:
   - Use the Elbow Method to plot inertia for `K` from 1 to 10.
   - Identify the "elbow" point (typically `K=5` for this dataset) and re-fit K-Means with the optimal `K`.

4. **Cluster Visualization**:
   - Plot clusters using the original features (`Annual Income` vs. `Spending Score`) with color-coding.
   - Plot clusters using PCA components for a 2D perspective.

5. **Evaluation**:
   - Compute the silhouette score for the chosen `K`.
   - Plot silhouette scores for a range of `K` values to confirm the optimal number of clusters.

## Example Output
```plaintext
Silhouette Score for K=5: 0.5539
Silhouette Score for K=2: 0.4322
Silhouette Score for K=3: 0.4983
Silhouette Score for K=4: 0.5321
...
```

### Visualizations
- **PCA Plot**: Shows the 2D distribution of customers after dimensionality reduction.
- **Elbow Plot**: Identifies the optimal `K` (typically 5) where inertia starts to level off.
- **Cluster Plot (Original Features)**: Displays clusters based on `Annual Income` and `Spending Score`.
- **Cluster Plot (PCA)**: Visualizes clusters in the PCA 2D space.
- **Silhouette Score Plot**: Confirms the optimal `K` with the highest silhouette score.

![Cluster Visualization Example](https://via.placeholder.com/600x400.png?text=Cluster+Visualization+Plot)

## Learning Outcomes
This project offers valuable learning opportunities for data analysts and machine learning practitioners:

- **Clustering Basics**: Understand how K-Means clustering segments data into meaningful groups.
- **Dimensionality Reduction**: Learn to use PCA for 2D visualization of high-dimensional data.
- **Optimal Cluster Selection**: Gain hands-on experience with the Elbow Method for choosing `K`.
- **Evaluation Metrics**: Explore the silhouette score to assess clustering quality.
- **Visualization Skills**: Create insightful plots to interpret clustering results.
- **Practical Application**: Apply clustering to a real-world dataset for customer segmentation.

## Key Insights
- **Customer Segments**: The optimal `K=5` reveals distinct customer groups (e.g., high income/high spending, low income/low spending, etc.).
- **Silhouette Score**: A score of ~0.55 for `K=5` indicates good clustering quality (closer to 1 is better).
- **Feature Importance**: `Annual Income` and `Spending Score` effectively separate customers into meaningful clusters.
- **Business Application**: These clusters can inform targeted marketing strategies, such as offering premium services to high-income, high-spending customers.
- **PCA Utility**: PCA helps visualize clusters in 2D, confirming the separability of customer groups.

## Future Improvements
- **Additional Features**: Incorporate `Age` and `Gender` for more nuanced clustering.
- **Advanced Clustering**: Experiment with other algorithms like DBSCAN or hierarchical clustering.
- **Interactive Visualizations**: Use Plotly for interactive cluster exploration.
- **Feature Engineering**: Create new features (e.g., income-to-spending ratio) to improve clustering.
- **Business Recommendations**: Add a section to interpret clusters for marketing strategies.

## Contributing
Contributions are welcome! If you'd like to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.


⭐ If you found this project helpful, please give it a star on GitHub! ⭐
