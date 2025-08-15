# customer-segmentation-project

# Customer Segmentation using K-Means Clustering

An unsupervised machine learning project that identifies distinct customer personas from a dataset based on their income and spending habits.

![Project Banner](https://i.imgur.com/vHqjHZF.png)

## 1. Project Objective

This project demonstrates an end-to-end workflow for **unsupervised learning**. Instead of predicting a known value, the goal is to discover hidden structures and natural groupings within a customer dataset. By identifying these distinct segments, a business can move from a "one-size-fits-all" marketing strategy to highly targeted campaigns tailored to different customer personas, improving engagement and profitability.

---

## 2. Dataset

The model uses the **Mall Customer Segmentation Data**, a popular and clean dataset from Kaggle, ideal for clustering tasks.

* **Source:** [Kaggle Dataset Link](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
* **Content:** Contains basic demographic and financial data for 200 mall customers, including `Age`, `Gender`, `Annual Income`, and a proprietary `Spending Score (1-100)`.

---

## 3. Methodology & Key Techniques

The project applies a standard methodology for unsupervised clustering to identify and interpret customer segments.

1.  **Exploratory Data Analysis (EDA):** The initial relationship between `Annual Income` and `Spending Score` was visualized using a scatter plot, which revealed the potential for distinct clusters.
2.  **Data Preparation:** The relevant features (`Annual Income` and `Spending Score`) were selected. **Feature Scaling** was applied using `StandardScaler`, a critical step for distance-based algorithms like K-Means.
3.  **Optimal Cluster Determination:** The **Elbow Method** was used to programmatically determine the optimal number of clusters (K) for the dataset. This involved iterating from 1 to 10 clusters and plotting the Within-Cluster Sum of Squares (WCSS).
4.  **K-Means Clustering:** A **K-Means** model was trained using the optimal K value (K=5). The algorithm assigned each customer to one of the five clusters.
5.  **Visualization & Interpretation:** The final clusters were visualized on a scatter plot, and the characteristics of each group were analyzed to define distinct customer personas.

---

## 4. Results & Customer Personas

The Elbow Method clearly identified **K=5** as the optimal number of clusters. The K-Means algorithm then successfully segmented the customers into the following five distinct personas:

![Final Customer Segments Plot](https://i.imgur.com/kYmZ6wN.png)

* **Cluster 0 (Green): Impulse Buyers** - Low income, but high spending scores.
* **Cluster 1 (Blue): Standard Customers** - The largest group, with average income and spending.
* **Cluster 2 (Orange): High-Value Targets** - High income and high spending. The most valuable segment for marketing.
* **Cluster 3 (Red): Savers** - High income, but low spending scores.
* **Cluster 4 (Purple): Cautious Spenders** - Low income and low spending scores.

---

## 5. Technologies Used

* **Python 3**
* **Pandas:** For data loading and manipulation.
* **Scikit-learn:** For the unsupervised learning pipeline, including `KMeans` and `StandardScaler`.
* **Matplotlib & Seaborn:** For data visualization, including the scatter plots and Elbow Method chart.
* **Jupyter Notebook / VS Code:** For the development environment.
