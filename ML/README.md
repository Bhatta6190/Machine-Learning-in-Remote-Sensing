# Hyperspectral Data Analysis, Principal Component Analysis and Clustering (K-Means) 

## Overview  
This work analyzes hyperspectral data collected by the **RIT MX1 drone** over the **RIT Tait Reserve**. The workflow includes:  

- **Data visualization**  
- **Principal Component Analysis (PCA)** for dimensionality reduction  
- **Noise reduction** using PCA  
- **K-Means clustering** on hyperspectral and Sentinel-2 multispectral data  

## Dataset  
The dataset consists of **ENVI-format hyperspectral images**:  
- `taitlabsphere` (image data)  
- `taitlabsphere.hdr` (metadata)  

## Methods  

### 1. Data Preprocessing & Visualization  
- Loaded the dataset using **Spectral Python (SPy)**.  
- Visualized RGB and false-color composites.  

### 2. Principal Component Analysis (PCA)  
- Used **Singular Value Decomposition (SVD)** for dimensionality reduction.  
- Visualized the top principal components and their variance contribution.  
- Analysis of PCA components and their contributions.
- Applied PCA-based **noise reduction** by reconstructing from principal components.  

### 3. K-Means Clustering  
- Implemented **K-Means clustering** on PCA-reduced features for simple *RGB image*, *Sentinel-2 multispectral image* and given *Hyperspectral image*.  
- Compared clustering performance across different feature dimensions (PCs) as well as its performance across different imgagery data.  

## Project Structure  
```plaintext
📂 hyperspectral-analysis
│── 📄 PCA_and_ML_code.ipynb    # Contains all code (PCA, visualization, clustering)  
│── 📄 README.md                # Project Explanation
```
<h2>Sample Results</h2>

<h3>1. HSI Data Visualization</h3>
<div class="image-container">
    <img src="./Results/HSI_RGB_image.png" alt="HSI RGB Image">
    <img src="./Results/HSI_CIR_image.png" alt="HSI CIR False Color Image">
</div>
<p><em>Explanation</em></p>

<h3>2. PCA Components</h3>
<img src="./Results/PCA_bands.png" alt="PCA Bands">
<p><em>Explanation</em></p>

<h3>3. Data Reconstruction</h3>
<img src="./Results/Target_reconstruction.png" alt="Spectra Reconstruction using PCA">
<p><em>Explanation</em></p>

<h3>4. 16-Bands Sentinel-2 Imagery Clustering</h3>
<div class="image-container">
    <img src="./Results/Sentinel-2 Imagery.png" alt="Sentinel-2 RGB Image">
    <img src="./Results/Clustered_sentinel_imagery.png" alt="K-Means Clustered Sentinel-2 Image">
</div>
<p><em>Explanation</em></p>

<h3>5. HSI Patch Reconstruction and Comparison</h3>
<div class="image-container">
    <img src="./Results/selected_HSI_patch.png" alt="HSI Patch Extraction">
</div>
<div class="image-container">
    <img src="./Results/hsi_kmeans_allbands.png" alt="Clustered Patch with All Bands">
    <img src="./Results/Hsi_patch_clustered_PCA.png" alt="Clustered Patch with PCA Reduced Data">
</div>
<p><em>Explanation</em></p>


