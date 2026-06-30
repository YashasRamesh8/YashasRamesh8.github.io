<!--
CHECKLIST FOR THIS PAGE (copy this file for each new project):
- [ ] Replace [YOUR PROJECT TITLE] with your project title
- [ ] Replace the hero image with your own (add to docs/assets/images/)
- [ ] Update the Overview section
- [ ] Update the Methods & Tools section
- [ ] Update the Key Findings section
- [ ] Update the Links section
- [ ] Add a card for this project on docs/projects/index.md
- [ ] Add a nav entry in mkdocs.yml
-->

![Forest Fire Risk Zonation Cover](../assets/images/project1-cover.png)

# Forest Fire Risk Zonation – Chikmagaluru District

**Category:** M.Tech Dissertation Project | **Institution:** Karnataka State Remote Sensing Applications Centre (KSRSAC), VTU | **Year:** 2023

---

## Objectives

- To prepare a Forest Fire Risk Zone (FFRZ) map of Chikmagaluru district using Multi-Criteria Decision Analysis (MCDA) techniques.
- To compare the results of Weighted Overlay Analysis (WOA) and Analytical Hierarchal Process (AHP) methods.
- To suggest measures to mitigate the impact of forest fires.

---

## Key Results & Findings

Ten thematic layers — covering vegetation, topography, anthropogenic, and climatic parameters — were integrated to first produce Forest Fire Vulnerability Zone (FFVZ) maps, which were then overlaid with projected population data to derive Forest Fire Risk Zone (FFRZ) maps. The results from both methods were validated against past fire incidence data from the Karnataka Forest Department (KFD), with a strong spatial correlation observed in high-risk zones.

### Weighted Overlay Analysis (WOA)

| Risk Zone | Area (Hectares) | Percentage |
|---|---|---|
| Low Risk | 17,343.62 ha | 52.64% |
| Moderate Risk | 9,263.49 ha | 28.11% |
| High Risk | 6,342.07 ha | 19.25% |

### Analytical Hierarchal Process (AHP)

| Risk Zone | Area (Hectares) | Percentage |
|---|---|---|
| Low Risk | 16,326.67 ha | 49.87% |
| Moderate Risk | 10,797.67 ha | 32.98% |
| High Risk | 5,613.30 ha | 17.15% |

Both methods produced comparable results, with a Consistency Ratio (CR) of 0.07 for AHP — well within the acceptable threshold of 0.1 — confirming the reliability of the parameter weightages. The close agreement between WOA and AHP demonstrates that field-knowledge-based weighting is as robust as the parametric AHP approach for this study area.

---

## Tools & Technologies Used

- **GIS Software:** ArcGIS 10.8 (Weighted Overlay, Raster Calculator, IDW), QGIS (Model Builder, Multiple Ring Buffer)
- **Remote Sensing:** Google Earth Engine, Cartosat DEM (Bhuvan Portal)
- **Data Sources:** KSRSAC, KSNDMC (meteorological data), Karnataka Forest Department (KFD), Projected Census Data
- **MCDA Methods:** Weighted Overlay Analysis (WOA), Analytical Hierarchal Process (AHP)
- **Spatial Operations:** Reclassification, IDW Interpolation, Buffer Analysis, Overlay Analysis

<!--
## Links

***
[View Code on GitHub](https://github.com/[YOUR-GITHUB-USERNAME]/[YOUR-REPO-NAME]){ .md-button }
[View Data Source](https://example.com){ .md-button }
***
-->
