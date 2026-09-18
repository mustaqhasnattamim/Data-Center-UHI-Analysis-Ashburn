# Quantifying the Urban Heat Island Effect of Hyperscale Data Center Construction (2015–2025)

<img width="5846" height="4134" alt="Layout" src="https://github.com/user-attachments/assets/4a4036e1-d58f-4ca6-a829-2a506d8bc5f5" />



## 📌 Overview
The rapid expansion of artificial intelligence and cloud computing has driven an unprecedented surge in hyperscale data center construction, physically transforming land cover and altering local microclimates. 

This project measures the exact thermal impact of an Amazon Web Services (AWS) data center campus in "Data Center Alley" (Loudoun County, VA) over a 10-year development lifecycle. Using Landsat Level-2 Surface Temperature imagery within ArcGIS Pro, surface heat changes were mapped across three temporal milestones: a pre-development baseline (2015), an active construction phase (2020), and a completed operational phase (2025).

## 🔬 Methodology
Raw satellite thermal data is highly susceptible to day-to-day atmospheric variations. To accurately isolate artificial land-use temperature changes from regional weather anomalies, a **Relative Normalization** methodology was applied. 

1. **Data Acquisition:** Landsat 8 and 9 Level-2 Surface Temperature (Band 10) imagery.
2. **Temperature Conversion:** Raster Math applied to convert satellite Digital Numbers to Celsius.
3. **Weather Calibration:** An undisturbed control forest was used as a baseline to calculate and subtract regional weather anomalies from the active temporal layers.
4. **Zonal Statistics:** Extracted the exact mean temperature increases within the digitized property boundaries of the AWS campus.

## 📊 Key Findings
The calibrated 10-year analysis confirmed a distinct thermal lifecycle tied to physical construction phases:

* **Phase 1: Clear-Cut & Construction (2015–2020):** Clearing vegetation and exposing bare dirt for construction generated a peak localized warming effect of **+4.00°C**.
* **Phase 2: Facility Completion (2020–2025):** The integration of high-albedo reflective metal roofs and water retention ponds mediated the extreme bare-dirt heat, yielding a minor sequential increase of **+0.82°C**.
* **Total Decade Impact (2015–2025):** Replacing the natural landscape with a hyperscale data center campus resulted in a permanent average surface temperature increase of **+3.73°C** inside the property boundary.

## 📂 How to Open This Project

Due to GitHub's file size limits, the 2GB ArcGIS Pro project folder has been compressed and split into 100MB multi-part 7-Zip files.

**To open the project on your local machine:**
1. Download **all** of the `.7z.00X` files (e.g., `.7z.001`, `.7z.002`, etc.) and place them into the same single folder on your computer.
2. Ensure you have [7-Zip](https://www.7-zip.org/) installed.
3. Right-click **ONLY** the first file in the sequence (`filename.7z.001`).
4. Select `7-Zip` > `Extract Here` (or `Extract to "folder\"`). 7-Zip will automatically detect the other parts and combine them into the full ArcGIS Pro project folder.
5. Open the `.aprx` file in **ArcGIS Pro**.

## 🛠️ Requirements
* ArcGIS Pro (Advanced License recommended for Spatial Analyst tools)
* 7-Zip (for extracting the project files)
