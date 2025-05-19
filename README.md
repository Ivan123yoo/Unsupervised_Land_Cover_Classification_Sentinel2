# Land Cover Classification Using Unsupervised Learning

## About This Project  
This project is a final assignment for GEOL0069 at University College London, exploring the use of remote sensing and unsupervised learning techniques for land cover classification. Using Sentinel-2 satellite imagery, it applies spectral indices (NDVI, NDWI, and SWI) and clustering algorithms (K-means) to analyze and distinguish various land cover types, including vegetation, water bodies, and natural features. The focus is on two contrasting regions — the Mississippi Delta and Patagonia — each presenting unique environmental characteristics and classification challenges.

## Project Objectives  
- Utilize NDVI, NDWI, and SWI for initial land cover characterization, capturing vegetation health, water presence, and enhanced water detection.  
- Apply K-means clustering (an unsupervised method) to categorize land cover types without requiring labeled data.  
- Explore how spectral characteristics vary across two diverse regions — Mississippi, with its river networks and coastal zones, and Patagonia, with its mountainous terrain and complex water systems.  
- Provide a clear and well-documented workflow for land cover classification using Python.  

## Background and Context  
Land cover classification is essential for environmental monitoring, enabling better understanding of ecosystem dynamics, resource management, and sustainable land use. However, accurately distinguishing land cover types can be challenging due to mixed pixels, complex landscapes, and variable environmental conditions. Traditional supervised methods require labeled data, which is often unavailable, especially for remote regions. 

This project addresses these challenges using Sentinel-2 imagery, which provides high-resolution, multi-spectral data suitable for detailed land cover analysis. By combining NDVI, NDWI, and SWI — each tailored to detect specific land features — with unsupervised K-means clustering, this project demonstrates a scalable approach to efficiently classify diverse landscapes without the need for labeled training data. 

### Study Regions
This methodology is tested on two regions that represent different classification challenges:  
- **Mississippi Delta:**  
  - Characterized by a complex river network, water channels, and coastal zones.  
  - Challenges include distinguishing water from land due to sediment and shallow waters.  

- **Patagonia:**  
  - A region of mountainous terrain, lakes, and dense vegetation.  
  - Challenges arise from the mix of snow, water, and forested areas, complicating classification.  

## Why This Approach Matters  
By integrating multiple spectral indices with unsupervised clustering, this project provides a scalable, adaptable solution for land cover classification in diverse regions. The workflow can be applied to other geographic areas, making it a versatile tool for environmental research and data science.  


## Sentinel-2 Satellite Imagery

Sentinel-2 is a European Earth observation mission providing high-resolution, multi-spectral imagery, making it ideal for environmental analysis. This project uses Sentinel-2 data to classify land cover types in two contrasting regions: Mississippi and Patagonia. The choice of Sentinel-2 is due to its high spatial resolution (10m, 20m, and 60m) and its extensive spectral range, covering 13 bands from visible to short-wave infrared.

In this project, specific bands are used for targeted land cover analysis. NDVI (Normalized Difference Vegetation Index) is calculated using the Red (Band 4) and Near-Infrared (NIR - Band 8) bands, highlighting vegetation. NDWI (Normalized Difference Water Index) uses the Green (Band 3) and NIR bands to detect water bodies. Additionally, SWI (Spectral Water Index) applies the Red Edge (Band 5) and Short-Wave Infrared (SWIR - Band 11) bands, providing enhanced water classification.

The use of Sentinel-2 imagery allows for consistent and accurate land cover detection across both regions. Its high-resolution, multi-spectral capabilities ensure that vegetation, water bodies, and other features are accurately identified, making it the foundation of this project’s classification process.

** NDWI analysis**
<img width="1046" alt="Screenshot 2025-05-17 at 12 50 08" src="https://github.com/user-attachments/assets/c88187b0-12b7-483d-9e11-947798afdb78" />

## NDWI Calculation Using Sentinel-2 MSI Imagery

The **Normalized Difference Water Index (NDWI)** is a remote sensing technique used to detect water bodies in satellite imagery. It is calculated using the Green (B3) and Near-Infrared (NIR) (B8) bands from Sentinel-2 MSI imagery. 

### NDWI Formula:
$$
\text{NDWI} = \frac{\text{Green - NIR}}{\text{Green + NIR}}
$$

### Why These Bands?
The Green Band (B3) is highly reflective for water bodies, making it useful for distinguishing water from vegetation. The Near-Infrared (NIR) Band (B8) is absorbed by water but strongly reflected by vegetation, creating a strong contrast.

### What the Figure Shows:
The MSI (MultiSpectral Instrument) on the Sentinel-2 satellite captures reflected light across multiple bands, including Green (B3) and NIR (B8). These bands are used to calculate NDWI, with high values indicating water (green in the images) and low values indicating land (red in the images). 

The figure highlights the NDWI results for two regions: 
Mississippi, where green areas represent water bodies, while red areas show land. 
Patagonia, where high NDWI values show the water bodies, while land appears red.

### Applications:
NDWI is widely used in environmental monitoring, water resource management, and flood mapping.

### K-Means Clustering on Mississippi Region

This figure demonstrates the application of K-means clustering on a Sentinel-2 satellite image of the Mississippi region. The top section illustrates the concept of K-means clustering, where data points are categorized into distinct clusters. The lower section showcases the practical implementation: the original true color image of Mississippi is processed using K-means clustering, resulting in a classified image with four distinct clusters (k=4). This approach effectively segments the region into areas of similar characteristics, providing a clear visualization of different land cover types.

<img width="1021" alt="Screenshot 2025-05-18 at 16 05 54" src="https://github.com/user-attachments/assets/22b0f929-a195-4209-81c6-404db21e9ee7" />

## Step-by-step guide

This project was created using Google Colab for unsupervised land cover classification. Follow these steps to set it up:

1. **Download the Notebook:**  
   - Download `Unsupervised_Land_Cover_Classification.ipynb` from this repository.

2. **Get Sentinel-2 Images:**  
   - Ensure you have Sentinel-2 images for Mississippi and Patagonia, including the necessary bands (Red, NIR, Green, Red Edge, SWIR).

3. **Set File Paths:**  
   - Modify file paths in the Colab notebook to match your image locations.

4. **Install Required Libraries:**  
   - Run the cell to install `rasterio`. Other libraries are pre-installed in Colab.

5. **Run the Code:**  
   - Execute the NDVI section for vegetation mapping.  
   - Execute NDWI and SWI sections for water detection.  
   - Run the K-means clustering section to classify land cover.

6. **Adjust K-means Clustering (Optional):**  
   - Change the value of `k` to test different cluster numbers (3, 4, 5, or 6).

7. **Save Processed Images:**  
   - Save the final NDVI, NDWI, SWI, and clustered images.

8. **Analyze Results:**  
   - Compare NDVI, NDWI, and SWI maps for both regions.  
   - Evaluate the impact of different k-values.

9. **Customize Further:**  
   - Modify clustering, add new spectral indices, or test other regions.



### Environmental Cost Assessment

This project’s environmental impact was calculated by assessing the energy consumption and carbon emissions associated with processing Sentinel-2 satellite data on Google Colab. The analysis accounted for data size, computational resources, and carbon emissions:

**Data Size:**  
- Total data processed: **35.95 MB**, including Sentinel-2 bands for Mississippi and Patagonia.

**Computational Resources:**  
- Platform: Google Colab Pro with T4 GPU (High RAM).  
- Total processing time: 50 hours.  
- Average power consumption of T4 GPU: 70 watts (W).  

**Energy Consumption and Carbon Emissions:**  
- Total energy consumption: 3.5 kWh (50 hours × 70 W).  
- Carbon intensity: 0.475 kg CO₂/kWh (average value).  
- Total carbon emissions: 1.66 kg CO₂.  

This result indicates a moderate environmental impact for the project. Although the total carbon emissions of 1.66 kg CO₂ are not excessively high, they highlight the importance of optimizing computational processes to minimize energy consumption.

## Project Demonstration Video

https://youtu.be/hFFw8sM8QG8

## Data Source

The Sentinel-2 satellite images used in this project were obtained from the Copernicus Open Access Hub, a part of the European Space Agency's (ESA) Copernicus Programme. These images provide high-resolution multispectral data, making them ideal for NDWI, NDVI, and clustering analyses.
A free account is required for these images to be downloaded.

## Additional Information

This project was developed using Google Colab Pro, which provided additional RAM and computational resources necessary for processing high-resolution Sentinel-2 imagery and performing clustering analysis efficiently.

## Acknowledgments

I would like to express my sincere gratitude to Dr. Michel Tsamados and Weibin Chen for their guidance and support throughout this project.

## References

Du, Y., Ling, F., Zhou, J., Wang, Q., Wen, D. and Guo, Y. (2016). 'Normalized Difference Vegetation Index (NDVI) based on Landsat 8 OLI imagery accurately monitors vegetation dynamics in a subtropical region', *Remote Sensing*, 8(3), pp. 1–14.

Gao, B. C. (1996). 'NDWI – A Normalized Difference Water Index for Remote Sensing of Vegetation Liquid Water from Space', *Remote Sensing of Environment*, 58(3), pp. 257–266.

Jiang, Z., Huete, A. R., Chen, Y., Chen, J. and Li, J. (2006). 'Analysis of NDVI and scaled difference vegetation index retrievals of vegetation fraction', *Remote Sensing of Environment*, 101(3), pp. 366–378.

MacQueen, J. (1967). 'Some Methods for Classification and Analysis of Multivariate Observations', *Proceedings of the Fifth Berkeley Symposium on Mathematical Statistics and Probability*, 1, pp. 281–297.

Ester, M., Kriegel, H.P., Sander, J. and Xu, X. (1996). 'A density-based algorithm for discovering clusters in large spatial databases with noise', *Proceedings of the Second International Conference on Knowledge Discovery and Data Mining*, pp. 226–231.

Richards, J. A. (2013). 'Remote Sensing Digital Image Analysis: An Introduction', *Springer Science & Business Media*.
