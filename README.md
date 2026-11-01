# UNSW-NB15 Network Traffic Clustering

## Project Overview

This project explores network traffic patterns using unsupervised machine learning techniques on the UNSW-NB15 dataset.

The objective is to identify groups of similar network traffic records without using attack labels during model training. The discovered clusters are then analyzed to understand their relationship with normal and malicious network traffic.

## Objectives

- Perform exploratory data analysis on network traffic.
- Prepare and preprocess numerical network features.
- Apply unsupervised machine learning algorithms.
- Visualize clusters using Principal Component Analysis (PCA).
- Compare clustering performance using the Silhouette Score.
- Analyze cluster composition using known attack labels.

## Dataset

**Dataset:** UNSW-NB15

The UNSW-NB15 dataset contains network traffic records representing normal activities and various types of network attacks.

The notebook uses:
- Four network traffic CSV files.
- A feature-description CSV file.
- Up to 5,000 records from each traffic file for the working sample.

**Dataset source:** [UNSW-NB15 Dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

The dataset files are not included in this repository. Download them from the original source before running the notebook.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Machine Learning Algorithms

### 1. K-Means Clustering
Groups network traffic records into clusters based on feature similarity.

### 2. Agglomerative Clustering
Uses a hierarchical clustering approach to group similar network records.

### 3. DBSCAN
Identifies dense groups of network traffic and detects records that do not belong to dense regions as noise.

## Project Workflow

1. Dataset loading
2. Data inspection and exploratory data analysis
3. Missing and infinite value handling
4. Numerical feature selection
5. Feature scaling using StandardScaler
6. K-Means clustering
7. Agglomerative clustering
8. DBSCAN clustering
9. PCA-based cluster visualization
10. Cluster profiling and comparison

## Evaluation Metrics

The project uses the following evaluation approach:

- **Silhouette Score:** Measures how well-separated the generated clusters are.
- **Cluster Distribution:** Examines the number of records assigned to each cluster.
- **Noise Analysis:** Examines records classified as noise by DBSCAN.
- **Cluster Composition:** Studies the distribution of known attack labels within clusters.

## Repository Structure

```text
UNSW-NB15-Network-Traffic-Clustering/
│
├── UNSW_NB15_Unsupervised_Learning_Furnished.ipynb
└── README.md
```

## How to Run

1. Download the UNSW-NB15 dataset.
2. Open the notebook using Google Colab or Jupyter Notebook.
3. Upload the required dataset CSV files.
4. Update the dataset file paths if necessary.
5. Execute the notebook cells in sequence.
6. Review the clustering results and visualizations.

## Key Learning Outcomes

- Understanding unsupervised machine learning.
- Applying different clustering algorithms.
- Understanding feature scaling and dimensionality reduction.
- Evaluating clustering performance.
- Interpreting network traffic patterns.

## Limitations

- The experiment uses a limited working sample rather than the complete dataset.
- Only numerical features are used for clustering.
- Clustering results do not directly represent confirmed attack classifications.
- DBSCAN performance depends on parameter selection.

## Future Improvements

- Experiment with the complete UNSW-NB15 dataset.
- Include appropriately encoded categorical features.
- Optimize DBSCAN parameters.
- Explore additional clustering algorithms.
- Evaluate cluster quality using external validation metrics.

## Disclaimer

This project is an academic machine learning experiment intended for educational and research purposes. It is not a production-ready network intrusion detection system.
