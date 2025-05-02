### Introduction
This report presents a concise analysis of a cluster of five **Mauzas** (revenue villages) in Tehsil Pabbi, District Nowshera, Khyber Pakhtunkhwa, Pakistan. The primary objective is to examine land use changes—specifically, the **conversion of agricultural land**—using both cadastral vector datasets and satellite imagery.

The analysis utilizes the original **agricultural parcels (Khasras)** created during the land record digitization process. These parcels were overlaid with **median NDVI values** calculated for the period **January 1, 2024 to December 31, 2024**, derived from Sentinel-2 Harmonized satellite imagery. Based on this NDVI assessment, it is estimated that approximately **19%** of agricultural land has transitioned to non-agricultural use.

---

### Objectives
1. Visualize the cadastral (vector) datasets of the five Mauzas on an interactive map.
2. Display key land use types (e.g., agriculture, built-up areas, roads) in separate layers.
3. Generate a median NDVI layer using **Sentinel-2 Harmonized (10m resolution)** imagery over a one-year period.
4. Identify and visualize agricultural parcels with **median NDVI values between 0.3 and 0.7**, indicative of active cultivation.
5. Quantify the reduction in agricultural land area in **Kanal**.

---

### Datasets

- **Vector Data**  
  The cadastral vector dataset was provided by [Mr. Aftab Ahmad](https://www.linkedin.com/in/aftab-ahmad-4316a463/), Deputy Director GIS, Board of Revenue (BOR), KP. It includes agricultural field boundaries (*Khasras*) categorized as follows:

  | Land Use      | No. of Parcels | Area (Kanal, Approx.) |
  |---------------|----------------|------------------------|
  | Agriculture   | 5,795          | 32,729                 |
  | Stream        | 302            | 822                    |
  | Other         | 229            | 1,047                  |
  | Road/Street   | 172            | 1,668                  |
  | Graveyard     | 29             | 202                    |
  | Built-Up      | 24             | 602                    |

  > **Note:** This dataset is based on the manual land settlement records of 1926. Actual on-ground conditions may have changed since then.

- **Satellite Imagery**  
  - The study uses [Sentinel-2 Harmonized Surface Reflectance](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED) imagery, accessed via Google Earth Engine.
  - Images were filtered by region (five Mauzas), date range (2024), and cloud coverage (<10%).
  - A total of **135 images** were processed to compute NDVI values for the year 2024.

---

### Tools and Libraries Used
- **Google Earth Engine** – Satellite image processing and remote sensing analysis  
- **geemap** – Interactive mapping and Earth Engine integration in Python  
- **GeoPandas** – Spatial data manipulation in Python

---

### Assumptions
- Seasonal analysis (e.g., **Rabi** and **Kharif**) has not been performed. Instead, the study uses a one-year aggregated NDVI analysis to represent changes in agricultural land use.

---

### Findings
- A total of **4,473 agricultural parcels** were identified with **median NDVI values below 0.3**, suggesting possible conversion to non-agricultural uses.
- The total **agricultural area** has declined from **32,729 Kanal** to **26,359 Kanal**, indicating a **19% reduction** in cultivated land since the 1926 settlement.

---

### Results
![Result](https://github.com/code4geoai/gee/releases/download/0.3/Pabbi_Mauzas.Analysis.png)

