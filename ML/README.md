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
│── 📂 Results/                 # Contains sample of generated figures and analysis
```

## Sample Results

### 1. HSI Data Visualization
<p align="left">
  <img src="./Results/HSI_RGB_image.png" alt="HSI RGB Image" width="40%"/>
  <img src="./Results/HSI_CIR_image.png" alt="HSI CIR Image" width="40%"/>
</p>
<p align="center"><strong>Figure:</strong> RGB (left) and CIR false-color (right) imagery extracted from HSI data.</p>

### 2. PCA Components
<p align="center">
  <img src="./Results/PCA_bands.png" alt="PCA Components" width="125%"/>
</p>
<p align="center"><strong>Figure:</strong> PCA components extracted from the hyperspectral image.</p>

### 3. Data Reconstruction
<p align="center">
  <img src="./Results/Target_reconstruction.png" alt="Spectra Reconstruction using PCA" width="150%"/>
</p>
<p align="center"><strong>Figure:</strong> Spectral reconstruction using PCA.</p>

### 4. 16 Bands Sentinel-2 Imagery Clustering
<p align="left">
  <img src="./Results/Sentinel-2%20Imagery.png" alt="Sentinel-2 RGB Image" width="45%"/>
  <img src="./Results/Clusterd_sentinel_imagery.png" alt="Clustered Sentinel-2 Image" width="52%"/>
</p>
<p align="center"><strong>Figure:</strong> Sentinel-2 RGB image (left) and clustered image using K-means (right).</p>

### 5. HSI Patch Reconstruction and Comparison
#### Selected HSI Patch:
<p align="center">
  <img src="./Results/selected_HSI_patch.png" alt="HSI Patch Extraction" width="90%"/>
</p>
<p align="center"><strong>Figure:</strong> Extracted 250x250 HSI patch (right).</p>

#### Clustered Patch Comparison:
<p align="left">
  <img src="./Results/hsi_kmeans_allbands.png" alt="Clustered All Bands" width="48%"/>
  <img src="./Results/Hsi_patch_clustered_PCA.png" alt="Clustered PCA" width="48%"/>
</p>
<p align="center"><strong>Figure:</strong> Clustered patch using all bands (left) vs. PCA-reduced data (right).</p>



