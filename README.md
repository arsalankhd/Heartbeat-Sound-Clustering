# 🎧 Heartbeat Sound Clustering

## 📝 Overview

This project explores heartbeat audio data using **unsupervised machine learning** to discover natural patterns and groupings within the sounds. Instead of predicting predefined labels, this analysis uses clustering algorithms to segment the heartbeat recordings based on their intrinsic properties. The core of the project involves extracting meaningful features from audio signals and then applying and comparing different clustering techniques to understand the underlying structure of the data.

The entire workflow is implemented in the `heartbeat_clustering.ipynb` notebook.

---

## 📊 Dataset

The project uses the **Heartbeat Sounds** dataset from [Kaggle](https://www.kaggle.com/datasets/shayanfazeli/heartbeat). This dataset contains a collection of heartbeat audio files in `.wav` format, which are ideal for signal processing and feature extraction.

---

## 🛠️ Project Workflow

The analysis was conducted in a sequence of well-defined steps:

### 1. **Audio Feature Extraction**
- The `librosa` library was used to load each audio file.
- **Mel-Frequency Cepstral Coefficients (MFCCs)** were extracted from each audio signal. MFCCs are powerful features that capture the timbral and spectral characteristics of a sound, making them highly effective for audio analysis tasks.

### 2. **Dimensionality Reduction with PCA**
- The extracted MFCC feature vectors have high dimensionality.
- To enable visualization and improve the performance of clustering algorithms, **Principal Component Analysis (PCA)** was applied to reduce the feature space to two principal components.

### 3. **Clustering Analysis**
Two distinct clustering algorithms were applied to the 2D feature set to compare their effectiveness:

- **K-Means Clustering**: This algorithm partitions the data into a pre-defined number of clusters (`k`). It's effective for identifying spherical, well-separated groups.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: This algorithm groups together points that are closely packed, marking as outliers points that lie alone in low-density regions. It's powerful because it doesn't require the number of clusters to be specified beforehand and can find arbitrarily shaped clusters.

### 4. **Visualization and Comparison**
- The results from both K-Means and DBSCAN were visualized using scatter plots.
- These plots show how each algorithm grouped the heartbeat sounds in the 2D space, providing a clear visual comparison of their different approaches and outcomes.

---

## 🚀 Conclusion

This project successfully demonstrated a complete unsupervised learning pipeline for audio data. By extracting MFCC features, reducing their dimensionality, and applying both K-Means and DBSCAN, it was possible to identify distinct clusters within the heartbeat sounds. The comparison revealed the different strengths of each algorithm: K-Means for simple partitioning and DBSCAN for density-based grouping and outlier detection.

---

## 💻 Technologies Used

- Python 3
- Librosa (for audio processing)
- Scikit-learn (for PCA, K-Means, DBSCAN)
- Pandas & NumPy
- Matplotlib & Seaborn
- Jupyter Notebook

---

## ⚙️ How to Run

1.  Clone this repository.
2.  Install the required libraries:
    ```bash
    pip install librosa scikit-learn pandas numpy matplotlib seaborn jupyterlab
    ```
3.  Open the `heartbeat_clustering.ipynb` file in Jupyter.
