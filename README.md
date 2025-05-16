# Land Cover Classification Using Unsupervised Learning

## About This Project

This project is a final assignment for GEOL0069 at University College London, focusing on the application of unsupervised learning techniques to classify land cover types in two contrasting regions: Mississippi and Patagonia. Using Sentinel-2 satellite imagery, the project explores the use of spectral indices (NDVI, NDWI, and SWI) and clustering algorithms (K-means and DBSCAN) to identify and analyze various land cover categories, including vegetation, water bodies, and other natural features.

### Project Objectives
- Utilize NDVI, NDWI, and SWI for initial land cover characterization.
- Apply unsupervised clustering (K-means and DBSCAN) to classify land cover types.
- Compare the land cover characteristics between two diverse regions: Mississippi and Patagonia.
- Provide a clear and well-documented workflow for unsupervised land cover classification using Python.

## Background and Context

Land cover classification is a vital tool in environmental monitoring, enabling researchers and decision-makers to understand ecosystem changes, manage natural resources, and develop sustainable land management practices. Sentinel-2 satellite imagery offers high-resolution, multi-spectral data, making it ideal for detailed land cover analysis. By combining this data with unsupervised learning techniques, this project demonstrates how to efficiently classify land cover without requiring labeled data.

The significance of this project lies in its scalable approach. Unsupervised learning techniques, such as K-means and DBSCAN, allow for automated land cover classification in diverse regions. This can be applied to various environmental studies, including deforestation monitoring, water body mapping, and agricultural analysis. 

The code developed here can be easily adapted to other regions or datasets, making it a versatile tool for environmental researchers and data scientists. It provides a clear, adaptable framework for land cover classification using remote sensing and machine learning, benefiting both academic research and practical environmental management.

## Sentinel-2 Satellite Imagery

Sentinel-2 is a European Earth observation mission providing high-resolution, multi-spectral imagery, making it ideal for environmental analysis. This project uses Sentinel-2 data to classify land cover types in two contrasting regions: Mississippi and Patagonia. The choice of Sentinel-2 is due to its high spatial resolution (10m, 20m, and 60m) and its extensive spectral range, covering 13 bands from visible to short-wave infrared.

In this project, specific bands are used for targeted land cover analysis. NDVI (Normalized Difference Vegetation Index) is calculated using the Red (Band 4) and Near-Infrared (NIR - Band 8) bands, highlighting vegetation. NDWI (Normalized Difference Water Index) uses the Green (Band 3) and NIR bands to detect water bodies. Additionally, SWI (Spectral Water Index) applies the Red Edge (Band 5) and Short-Wave Infrared (SWIR - Band 11) bands, providing enhanced water classification.

The use of Sentinel-2 imagery allows for consistent and accurate land cover detection across both regions. Its high-resolution, multi-spectral capabilities ensure that vegetation, water bodies, and other features are accurately identified, making it the foundation of this project’s classification process.

