# Machine Learning in Remote Sensing

This repository provides tools and resources for applying machine learning to remote sensing data, enabling the generation of qualitative and quantitative data products. It covers tasks such as data cleaning, analysis, feature extraction, feature engineering, and outcome modeling across various remote sensing modalities, including multispectral, hyperspectral, and lidar data. The repository will be regularly updated with new tools and resources, as well as modifications to existing ones. Each directory below focuses on  specifics task of spectral data processing and Machine Learning and includes all necessary resources.

### Current Resources:

- **`EDA`**: `Exploratory Data Analysis (EDA)` of **Sentinel2** based  13 band `Multispectral` imagery collected over Rochester, New York.
- **`ML`**: Analysis of `Hyperspectral` Imagery and application of `Principal Component Analysis(PCA)` for dimensionality reduction and using the data for `K-means` clustering     based Unsupervised classification.
- **`HSI_classification_regression`**: Contains two directories as:

```
HSI_classification_regression/
│── Classification/    # Binary classification (Logistic Regression) & Multi-class classification (XGBoost) using Pavia University dataset  
│── Regression/        # Chlorophyll content prediction using Linear Regression, PLSR, and MLP with spectral band values as features  
```

Suggestions are highly appreciated.

For resource usage and potential collaborations, contact: rb1005@rit.edu.

we will use remote sensing dataset (PaviaU.mat and PaviaU gt.mat) to perform both
types of classification