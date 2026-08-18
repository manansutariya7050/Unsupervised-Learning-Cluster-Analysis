# Boston Housing Unsupervised Learning & K-Means Clustering

## Week 3 Internship Task

This project demonstrates a simple **unsupervised learning and clustering** workflow using the Boston Housing dataset and Python.

The main objective is to group similar housing observations using **K-Means clustering** without using a target variable during cluster formation.

## Dataset

- File: `BostonHousing.csv`
- Rows: 506
- Columns: 14
- Target/value column: `medv`
- Clustering features: rm, lstat, ptratio, crim

The `medv` column is excluded from clustering because it represents median house value. It may be compared after clustering to help interpret the resulting groups.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Project Workflow

1. Load the dataset
2. Inspect the dataset
3. Check missing values and duplicates
4. Handle missing numerical values using median imputation
5. Select simple clustering features
6. Standardize the features
7. Compare K values using the Elbow Method
8. Calculate Silhouette Scores
9. Apply K-Means clustering
10. Visualize the clusters
11. Analyze cluster sizes
12. Compare average cluster characteristics
13. Save the clustered dataset

## Clustering Method

### K-Means

K-Means was selected because it is simple, widely used, and easy to interpret for basic customer or geographic segmentation tasks.

The analysis evaluates K values from 2 to 6.

```python
KMeans(n_clusters=k, random_state=42, n_init=10)
```

## Features Used

The clustering uses:

- `rm`
- `lstat`
- `ptratio`
- `crim`

These features were standardized before applying K-Means.

## Why MEDV Is Excluded

`medv` represents median house value and is treated as an outcome/value variable. It is therefore not used to create the clusters.

After clustering, `medv` can be compared between clusters to understand their economic characteristics without influencing the clustering itself.

## Visualizations

The project includes:

- Elbow Method plot
- Silhouette Score plot
- Cluster scatter plot
- Cluster-size bar chart

## Repository Structure

```text
Boston-Housing-Clustering/
│
├── BostonHousing.csv
├── Week_3_BostonHousing_Clustering.ipynb
├── BostonHousing-Clustered.csv
├── Week_3_Boston_Housing_Clustering_Report.docx
├── README.md
└── images/
    ├── 01_elbow_method.png
    ├── 02_silhouette_scores.png
    ├── 03_cluster_scatter.png
    └── 04_cluster_sizes.png
```

## Running the Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn
```

Open Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

`Week_3_BostonHousing_Clustering.ipynb`

Run the cells from top to bottom.

## Results

The K-Means algorithm divides the housing observations into groups based on similarities in the selected neighborhood characteristics. Cluster profiles can then be compared using their average feature values.

## Skills Demonstrated

- Unsupervised learning
- K-Means clustering
- Data preprocessing
- Missing-value handling
- Feature scaling
- Elbow Method
- Silhouette Score
- Data visualization
- Cluster interpretation
- Python and Scikit-learn

## Internship Task

**Week 3 – Unsupervised Learning and Clustering Analysis**
