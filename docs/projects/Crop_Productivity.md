<!--
CHECKLIST FOR THIS PAGE (copy this file for each new project):
- [ ] Replace [YOUR PROJECT TITLE] with your project title
- [ ] Replace the hero image with your own (add to docs/assets/images/) — currently skipped
- [ ] Update the Overview section
- [ ] Update the Methods & Tools section
- [ ] Update the Key Findings section
- [ ] Update the Links section
- [ ] Add a card for this project on docs/projects/index.md
- [ ] Add a nav entry in mkdocs.yml
-->

# Crop-Water Productivity – Tungabhadra Left Bank Canal Command Area

**Category:** Internship Project | **Institution:** Advanced Centre for Integrated Water Resources Management (ACIWRM) | **Year:** 2023

---

## Objectives

- To optimise the use of rainwater for increased crop production.
- To maximise the utilisation of existing irrigation schemes in a sustainable manner.
- To support the design of new irrigation schemes on sustainable principles.
- To develop practical tools to enhance Crop Water Productivity (CWP) under any irrigation condition.

---

## Area Description

The study was carried out for the **Tungabhadra Left Bank Canal (TBLB) irrigation system**, a reservoir-based protective irrigation scheme on the Tungabhadra River — a tributary of the Krishna River — in the State of Karnataka. The analysis focused on the project's two dominant water-consuming crops, **paddy and sugarcane**, which together occupy a significant share of the command area's cropped land while drawing a disproportionately high share of available irrigation water.

---

## Methodology

Crop Water Productivity was estimated using **PySEBAL**, a Python implementation of the Surface Energy Balance Algorithm for Land (SEBAL), which derives spatially explicit Actual Evapotranspiration (ETa) maps from remotely sensed satellite imagery. The workflow combined satellite, meteorological, and soil datasets to compute ETa, biomass production, and ultimately water productivity at the pixel level.

**Data acquisition**

- **Satellite imagery (Landsat):** Sourced from USGS EarthExplorer for the relevant path/row, used as the primary input to the SEBAL energy balance model.
- **Meteorological data (GLDAS):** Wind, temperature, humidity, and shortwave radiation (instantaneous and daily) downloaded from NASA's GES DISC portal for the study period.
- **Soil data:** Saturated/residual soil moisture content, field capacity, and wilting point retrieved from the HiHydroSoil dataset via a custom Google Earth Engine (JavaScript) script, written specifically to reduce the time required to download each soil layer compared to manual extraction.

**Model setup**

PySEBAL inputs were organised into a structured Excel workbook with four sheets — General, Meteorological, Soil, and Landsat input — each populated with file paths and image-specific parameters (Landsat number, thermal band, percentile thresholds for cold-pixel and NDVI-hot-pixel selection, and temperature lapse rate). The number of rows in the Landsat input sheet corresponded to the number of satellite images processed in a single run.

The model was executed via `Run_py3.py`, with the script's start/end row parameters set to batch-process the prepared image set. PySEBAL's built-in aggregation and gap-fill utility was then used to perform monthly aggregation, filtering, and temporal–spatial interpolation across the individual run outputs.

**Outputs derived**

- Actual and reference evapotranspiration (ETa, ETo)
- Crop transpiration and evaporation deficit
- Leaf Area Index (LAI) and biomass deficit
- Above Ground Biomass Production (AGBP) and Biomass Water Productivity
- Harvest index and yield, validated against ground-truth observations
- Final Water Productivity surface at 30 m resolution

---

## Tools & Technologies Used

- **Modelling:** PySEBAL (Surface Energy Balance Algorithm for Land, Python implementation)
- **Remote Sensing Data:** Landsat 7/8 (USGS EarthExplorer), GLDAS meteorological data (NASA GES DISC), HiHydroSoil soil data (Google Earth Engine)
- **GIS Software:** QGIS — used for visualising water resources and irrigation infrastructure, mapping crop-water use, and overlaying irrigation areas with DEM to identify drainage and waterlogging issues
- **Scripting:** Python (PySEBAL execution), JavaScript / Google Earth Engine (automated soil-layer extraction)
- **Spatial Operations:** DEM-based terrain analysis, gap-filling and temporal interpolation, ground-truth validation of yield and harvest index

---

## Key Takeaways

- Implemented a full satellite-to-yield pipeline — from raw Landsat and meteorological inputs through to a spatially explicit Water Productivity map — using an open-source SEBAL implementation.
- Automated a previously manual soil-data download process using a custom Earth Engine script, reducing the time needed to assemble model inputs.
- Applied QGIS alongside the PySEBAL outputs to connect water productivity results back to irrigation infrastructure, supporting practical recommendations on irrigation efficiency, water management, and crop selection for the TBLB command area.

---

[View Full Internship Report (PDF)](../assets/INTERNSHIP%20ACIWRM.pdf){ .md-button }