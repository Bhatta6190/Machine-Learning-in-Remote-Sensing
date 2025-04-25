# Exploratory Data Analysis (EDA) of Sentinel2 Multispectral Satellite Data

**Sentinel2** is a Earth observation mission satellite that capture 13 band imagery at various spatial resolution (from 20m to 60m). In this data analysis we will explore a dataset collected by this platform over Rochester, New York. The zip version of the dataset is also uploaded with the resource materials.

The code `eda.ipynb` does following serially:

- **Importing the data:** The Sentinel2 dataset is imported as numpy data, which is an array type data format in `python`. The data is 12 Bands. The original Sentinel2 data have 13 bands in this dataset we only have 12 as Band 10 (1375 nm) has been excluded.
- **Data Cleaning and Visualization:** Generally remote sensing data have low contrast, so for visualization purpose the data is contrast stretched using `percentile-stretching` techinque.
- **Band Statistics Analyis and Data Standarization:** Various band statistics are calculated for each bands like mean, standard deviation and Quartile. These helps to get the idea about band information content. `Data Standarization` is a common technique in ML which converts any data into z-score values. So the data is made to be in certain range of values.
- **Anamolies Visualization:** Z-scores values can be used to determine the outliers in the data by making a band distribution to be in certain z-score limit. Outside the limit, the values can be considered outliers.
- **Correlation and Density Analysis:** Correlation between bands helps one to know relation between bands and also what values of the samples contribute to the band most as well as least using Density analysis.In this code `Pearson Correlation Coefficient` is used for correlation analysis and `Gaussian KDE` for density analysis.
- **Spectral Matching using Spectal Angle Mapper (SAM):**`Spectral Angle Mapper (SAM)` is a technique in which pixels in the image are compared with the `Target spectrum` using `Cosine Similarity` metrics. The pixels with highest match will have lowest Cosine Angle and vice-versa. This is the simple method to determine the locations in the scene where our target is present. In this code we used `Oak tree (Genus: Quercus)` and `Constrution Asphalt` as target spectra to find their location in the Sentinel Imagery.

More information on Sentinel2 bands can be obatained from: https://gisgeography.com/sentinel-2-bands-combinations/                                                            
Target Spectra can be downloaded from: https://speclib.jpl.nasa.gov/library

🔴 **Note:** Download the code or use these links to view with Github Dev Tool:
- [`Click here`](https://github.dev/Bhatta6190/Machine-Learning-in-Remote-Sensing/blob/main/EDA/eda.ipynb) to view `eda.ipynb` file.