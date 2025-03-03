# Lombardy Snow Covered Areas Analysis

![SummerAndWinter](https://github.com/user-attachments/assets/30f67f70-8945-4acd-a967-3bfa20434049)


## Overview

This project analyzes the snow-covered areas in the Alps located in the northern region of Lombardy during winter and summer. The study leverages Sentinel-2 satellite imagery and the Normalized Difference Snow Index (NDSI) to assess seasonal snow coverage and its implications for water resource management, climate change studies, and disaster risk assessment.

## Author

**Bahman Amirsardary**\
Email: [bahman.amirsardary@mail.polimi.it](mailto\:bahman.amirsardary@mail.polimi.it)

## Objectives

- Analyze the extent of snow coverage in winter and summer.
- Assess the impact of seasonal snowmelt on water resources.
- Provide insights for climate studies, flood risk management, and policy-making.

## Methodology

### Data Collection

- **Satellite Data:** Sentinel-2 imagery from the Copernicus platform.
- **Image Selection:** L2A images (atmospherically corrected) with minimal cloud coverage.
- **Timeframe:**
  - Winter: December 2022 – February 2023 (6 images)
  - Summer: June 2023 – August 2024 (4 images)
- **Region of Interest:** Lombardy, Italy.

### Snow Detection Using NDSI

- **Formula:**
  
  {NDSI} = {Green Band (B3) - SWIR Band (B11)} / {Green Band (B3) + SWIR Band (B11)}
  
- **Threshold:** 0.4 (values above indicate snow coverage)
- **Cloud Differentiation:** Snow absorbs short-wave infrared but reflects visible light, while clouds reflect both.

### Processing Steps

1. **Preprocessing in QGIS:**
   - Mean snow coverage calculated for winter and summer using Raster Calculator.
   - Clustering of seasonal mean snow cover using the SAGA plugin.
   - Raster to vector transformation using the Polygonize tool.
2. **Spatial Analysis:**
   - Clipping the snow polygons with the Lombardy region boundary.
   - Removing misclassified areas (e.g., lakes misidentified as snow).
   - Calculating the area of each snow polygon.
3. **Comparative Analysis:**
   - Snow coverage in summer subtracted from winter to determine seasonal snowmelt.

## Results

- **Winter Snow Coverage:** 3503 km²
- **Summer Snow Coverage:** 1526 km²
- **Melted Snow Area:** 1977 km²
- **Potential Applications:**
  - Estimating the volume of water generated from melted snow.
  - Supporting resource management and policy planning.
  - Enhancing flood risk assessment and disaster management.

## Future Work

- Integrating Synthetic Aperture Radar (SAR) data for snow depth estimation.
- Assessing long-term snow cover trends using multi-year datasets.
- Investigating the correlation between snowmelt and downstream water levels.

## Tools and Technologies

- **Satellite Data:** Sentinel-2 (Copernicus)
- **Processing Software:** QGIS, SAGA GIS
- **Programming Languages:** Python (optional for automation and advanced analysis)

## Citation

If you use this work in your research, please cite:

> Bahman Amirsardary, "Lombardy Snow Covered Areas during Summer and Winter", Politecnico di Milano, 2024.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any questions or collaboration opportunities, feel free to reach out to [bahman.amirsardary@mail.polimi.it](mailto\:bahman.amirsardary@mail.polimi.it).



## Contact
For any questions or collaboration opportunities, feel free to reach out to [bahman.amirsardary@mail.polimi.it](mailto:bahman.amirsardary@mail.polimi.it).

