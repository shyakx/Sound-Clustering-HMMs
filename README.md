# README: Clustering Sound Images - Steven SHYAKA

## 📘 **Clustering Sound Images Using PCA and t-SNE**

## 🎯 Objective

This project aims to process and cluster sound data represented as images (likely spectrograms) using machine learning techniques, particularly **Principal Component Analysis (PCA)** and **t-distributed Stochastic Neighbor Embedding (t-SNE)**. These dimensionality reduction techniques help visualize and explore potential patterns in the feature space of sound image data.

---

## 📁 Dataset

The dataset consists of sound images (e.g., `.jpg`, `.png`) stored in a directory named `sound_images`. These images are expected to be visual representations of audio (e.g., spectrograms or mel-spectrograms).

---

## 📌 Key Dependencies

The following Python libraries are used:

* `os`, `glob`, `random`: for file handling and shuffling
* `matplotlib`, `seaborn`, `PIL`: for image processing and visualization
* `numpy`, `pandas`: for data manipulation
* `sklearn.decomposition.PCA`, `sklearn.manifold.TSNE`: for dimensionality reduction
* `tqdm`: for progress bars

---

## 📜 Workflow

### 1. **Setup & Imports**

All necessary libraries are imported and configured. This includes tools for loading images, visualizing them, and applying machine learning methods.

---

### 2. **Image Loading and Preprocessing**

* Images are loaded from the folder using `glob`.
* Only image files with the correct extensions are considered.
* Each image is:

  * Converted to grayscale.
  * Resized to a standard shape (64x64).
  * Flattened into a 1D feature vector.

> 📌 Output: A `features_array` matrix of shape (n\_samples, n\_features), where each row represents a processed image.

---

### 3. **Data Shuffling**

The image features and filenames are shuffled using the same seed to ensure reproducibility.

---

### 4. **PCA for Dimensionality Reduction**

* PCA reduces the high-dimensional image vectors to 50 principal components.
* This helps in retaining most variance while reducing dimensionality.
* Scree plot is generated to visualize the explained variance ratio.

---

### 5. **t-SNE for Visualization**

* t-SNE further reduces the PCA-transformed data to 2 dimensions.
* This makes it possible to plot and visually inspect clusters in 2D.
* A scatter plot is generated with thumbnails of corresponding sound images at their 2D positions.

---

### 6. **Cluster Visualization**

* A `visualize_tsne_with_images` function is defined and used to overlay the actual images at the points obtained from t-SNE for visual pattern inspection.
* The final output visually groups similar sounds based on their image representation.

---

## 🧠 Concepts Used

* **PCA**: Reduces dimensionality by projecting data onto directions of maximum variance.
* **t-SNE**: Non-linear technique for reducing data to 2 or 3 dimensions for visualization, preserving local structure.
* **Image Flattening**: Necessary to convert 2D image data into a vector suitable for ML models.

---

## 📊 Outputs

* A Scree Plot showing explained variance per PCA component.
* A 2D t-SNE scatter plot with sound images visually embedded at their cluster positions.

---

## 🔀 How to Use

1. Upload your sound image dataset in the expected folder (`sound_images/`).
2. Run the notebook step by step.
3. Observe the clustering results in the final scatter plot.
4. Use the plots to explore patterns, similarities, or anomalies in your sound image data.

---

## 📌 Note

Ensure that:

* All images are of uniform type (e.g., spectrograms).
* File sizes and dimensions are reasonable for the memory capacity of Colab.

---

## 🡩‍💻 Author

**Steven SHYAKA**
Software Engineering Student | Sound & AI Enthusiast
📍 Kigali, Rwanda
