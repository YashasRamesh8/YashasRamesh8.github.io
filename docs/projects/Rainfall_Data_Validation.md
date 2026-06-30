# Rainfall Data Validation & GIS Mapping – Tungabhadra Region

**Category:** Internship Project | **Institution:** Advanced Centre for Integrated Water Resources Management (ACIWRM) | **Year:** 2023

---

## Objectives

- To understand and apply standard procedures for validating raw rainfall records from field stations.
- To identify and flag discrepancies between Standard Rain Gauge (SRG) and Autographic Rain Gauge (ARG) observations at the same station.
- To plot and geo-reference raingauge station locations for the Tungabhadra basin using QGIS and ArcGIS.

---

## Background

Rainfall is the most frequently measured hydro-meteorological variable in India, yet raw records routinely contain gaps, transcription errors, and instrument inconsistencies. The India Meteorological Department (IMD) maintains the primary rain-gauge network, but water-resources projects at remote locations often rely on data from state agencies — the Water Resources Department, Agricultural Department, Disaster Management Department, and universities — adding further variability. A structured validation workflow is therefore essential before rainfall data is used in runoff modelling, flood forecasting, or irrigation planning.

---

## Methodology

### Data Validation Pipeline

Validation was carried out following a six-stage framework:

**Primary Validation → Secondary Validation → Data Correction & Completion → Data Compilation → Data Analysis → Data Reporting**

The three goals of any validation pass are:
1. Correct errors in recorded data wherever possible.
2. Assess reliability where correction is not possible.
3. Identify error sources to prevent recurrence.

### Primary Validation

Primary validation compares observations within a single data series against pre-set physical limits and expected hydrological behaviour. The key check applied here was a **SRG vs ARG comparison** — aggregating hourly ARG readings to daily totals and comparing them against the corresponding Standard Rain Gauge record. Days where the two readings diverged by more than 5% were flagged as suspect.

**Example — Aksheda Station, Pargaon Catchment (Sep–Oct 1996)**

A comparison of SRG and ARG daily records revealed significant discrepancies at multiple points during the monsoon and post-monsoon periods. Notable cases included:

| Date | SRG (mm) | ARG (mm) | % Difference |
|---|---|---|---|
| 3 Oct 1996 | 75.8 | 0.5 | −99.3% |
| 25 Sep 1996 | 3.8 | 13.5 | +255.3% |
| 17 Sep 1996 | 7.2 | 3.5 | −51.4% |
| 22 Oct 1996 | 0.7 | 1.5 | +114.3% |

These results illustrate the high spatial and temporal variability typical of monsoon-driven convective rainfall on the Indian subcontinent and the importance of cross-checking before data enters any model.

### Data Analysis Techniques

The following analytical methods were applied or studied for use in validation and reporting:

- Basic statistics (mean, standard deviation, range checks)
- Statistical tests for outlier detection
- Fitting of frequency distributions
- Flow duration series
- Regression analysis
- Rainfall Depth–Area–Duration analysis
- Rainfall Intensity–Frequency–Duration analysis

### GIS Mapping — Tungabhadra Region

Rain-gauge station locations for the Tungabhadra basin were plotted as point data and geo-referenced against a raster using **QGIS** and **ArcGIS**:

- An unrectified/un-georeferenced India rainfall raster was imported and spatially corrected.
- The raster was geo-referenced using 2015 annual rainfall data.
- Station point data was overlaid on a district-boundary shapefile of Karnataka to visualise spatial coverage within the area of interest.
- The mapped output confirmed that rainfall is at or above the expected maximum values for the Tungabhadra command area, consistent with its position on the wet leeward side of the Western Ghats.

---

## Tools & Technologies Used

- **GIS Software:** QGIS, ArcGIS — geo-referencing, point-data overlay, spatial visualisation
- **Data Sources:** IMD rain-gauge records (SRG and ARG), Karnataka State Remote Sensing Application Centre (KSRSAC) spatial data
- **Analysis:** Tabular and graphical SRG–ARG comparison, percentage-discrepancy computation, outlier flagging
- **Reference:** ACIWRM Rainfall Data Validation Manual

---

## Key Takeaways

- Applied the full ACIWRM data validation framework to real monsoon-season gauge records, learning to distinguish instrument error from genuine meteorological variability.
- Geo-referenced a historical India rainfall raster against point station data in QGIS/ArcGIS, producing a spatial view of gauge coverage across the Tungabhadra basin.
- Identified that discrepancies of ±100% between SRG and ARG at the same station are possible during convective events, reinforcing the need for systematic validation before any hydrological modelling.

---

[View Full Internship Report (PDF)](../assets/INTERNSHIP%20ACIWRM.pdf){ .md-button }
