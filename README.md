Clustering Unlabeled Sound Data
This repository contains a Jupyter Notebook (Clustering_Sound_Images_Steven_SHYAKA.ipynb) that demonstrates the process of clustering unlabeled sound data. The project involves loading audio files, extracting relevant features (MFCCs), performing dimensionality reduction using PCA and t-SNE, and applying clustering algorithms (K-Means and DBSCAN) to identify patterns in the sound data.

Table of Contents
Project Overview

Features

Setup

Usage

Data

Results and Observations

Dependencies

Author

Project Overview
The main goal of this project is to explore and cluster unlabeled sound data. This involves:

Data Loading and Feature Extraction: Loading .wav audio files and extracting Mel-frequency cepstral coefficients (MFCCs) as features.

Exploratory Data Analysis (EDA): Visualizing raw features to understand their distribution.

Dimensionality Reduction: Applying Principal Component Analysis (PCA) and t-Distributed Stochastic Neighbor Embedding (t-SNE) to reduce the dimensionality of the MFCC features for better visualization and clustering performance.

Clustering: Implementing K-Means and DBSCAN algorithms to group similar sound samples.

Evaluation: Assessing the quality of the clusters using metrics like Silhouette Score and Davies-Bouldin Index.

Visualization: Plotting the clusters in reduced-dimensional space to observe their separation.

Features
Audio Feature Extraction: Uses librosa to extract MFCCs.

Dimensionality Reduction: Implements PCA and t-SNE for effective data visualization.

Clustering Algorithms: Utilizes K-Means and DBSCAN for grouping similar sound data.

Cluster Evaluation: Provides quantitative metrics to evaluate clustering performance.

Interactive Visualizations: Generates scatter plots and pair plots to visualize data and clusters.

Setup
To run this notebook, you will need to have Python installed along with the necessary libraries.

Clone the repository (if applicable):

# If this project is part of a larger repository, provide clone instructions.
# git clone <repository_url>
# cd <repository_name>

Install dependencies:
It is recommended to use a virtual environment.

pip install -r requirements.txt

(If you don't have a requirements.txt file, you can create one with the following content based on the notebook's imports):

librosa
matplotlib
seaborn
pandas
numpy
scikit-learn

Download the data:
The notebook expects a unlabelled_sounds.zip file. Please ensure this file is placed in the specified path or update the unlabelled_data_path variable in the notebook.

unlabelled_data_path = "/content/drive/MyDrive/unlabelled_sounds.zip"

If running in Google Colab, ensure you mount your Google Drive as shown in the notebook:

from google.colab import drive
drive.mount('/content/drive')

Usage
Open the Jupyter Notebook:

jupyter notebook Clustering_Sound_Images_Steven_SHYAKA.ipynb

Or open it directly in Google Colab.

Run all cells:
Execute all cells in the notebook sequentially. The notebook is structured to guide you through the data loading, feature extraction, dimensionality reduction, clustering, and evaluation steps.

Explore the visualizations and observations:
The markdown cells contain explanations and observations regarding the results of each step.

Data
The project uses an unlabeled dataset of sound files, provided as unlabelled_sounds.zip. This zip file contains .wav audio files. The notebook extracts these files and processes them.

unlabelled_sounds.zip: Compressed archive containing .wav audio files.

Results and Observations
The notebook includes markdown cells where observations are documented. Key observations may include:

Raw Feature Visualization: Initial scatter plots and pair plots of raw MFCC features.

PCA Results: Explained variance ratio, scatter plots of PCA components, and the impact of PCA on data distribution.

t-SNE Results: Visualization of t-SNE embeddings, highlighting potential clusters.

K-Means Clustering: Cluster assignments, centroid locations, and evaluation metrics (Silhouette, Davies-Bouldin).

DBSCAN Clustering: Cluster assignments, noise points, and evaluation metrics.

Comparison of Algorithms: Discussion on the strengths and weaknesses of K-Means and DBSCAN for this dataset, especially concerning the need for pre-defined cluster numbers and handling of noise.

Real-World Applicability: Insights into the challenges of clustering real-world, high-dimensional, and noisy data.

Dependencies
The following Python libraries are used in this project:

librosa: For audio analysis and feature extraction.

matplotlib: For plotting and visualizations.

seaborn: For enhanced statistical data visualizations.

pandas: For data manipulation and analysis.

numpy: For numerical operations.

scikit-learn: For dimensionality reduction (PCA, t-SNE), clustering (K-Means, DBSCAN), and evaluation metrics.

zipfile: For handling zip archives.

Author
Steven SHYAKA
