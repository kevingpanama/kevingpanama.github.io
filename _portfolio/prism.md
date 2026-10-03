---
title: "PRISM: Panama Research and Integrated Sustainability Model"
excerpt: "Interactive geospatial dashboard of food security and child nutrition in Panama: ~100 province-level indicators from MINSA's national height censuses (2007, 2013) extracted from PDF reports and mapped with R, Quarto and Leaflet. Universidad Tecnológica de Panamá · APANAC 2023.<br/>[Open the dashboard](/PRISM/dashboard.html)"
collection: portfolio
order: 1
---

**Team:** K. González, E. Aguilar, A. G. Aizprúa, E. Cedeño, J. E. Sánchez-Galán (Universidad Tecnológica de Panamá)

**[Open the interactive dashboard →](/PRISM/dashboard.html)** · [Source code](https://github.com/kevingpanama/kevingpanama.github.io/tree/main/PRISM) · Paper: [APANAC 2023](/publication/2023-09-15-sistema-de-informacion-geoespacial-seguridad-alimentaria) (in Spanish) ([PDF](/files/gonzalez-ortega-2023-apanac-sistema-geoespacial.pdf), [DOI](https://doi.org/10.33412/apanac.2023.3959))

## The problem

Food security and child nutrition are central to poverty in Panama, but the data on them was locked in **unstructured PDF reports** from the Ministry of Health's (MINSA) Nutrition Program. No geospatial system showed where nutritional problems and interventions were concentrated.

## What we built

**PRISM** (Panama Research and Integrated Sustainability Model) is a geographic information system that brings layers of data about Panama together for interdisciplinary analysis, such as water quality, biological connectivity and biodiversity. Our contribution is its **nutrition and human health layer**:

1. **Web scraping** of MINSA Nutrition Program reports.
2. **Table extraction** from the PDFs with Tabula, then consolidation with pandas.
3. **Geospatial join** of the indicators with provincial and *comarca* boundaries using ISO 3166-2 codes, exported to GeoJSON.
4. **Interactive dashboard:** choose an indicator and the map recolors each province on a viridis scale, with a tooltip showing each province's value.

## Indicators

The data covers **96 indicators (2003–2014)** from the VI (2007) and VII (2013) National Height Censuses of first-grade schoolchildren and MINSA's 2016 report on nutrition in population groups, including:

* Census coverage of schoolchildren aged 6–9
* Mean and median height of 7-year-old boys and girls
* Prevalence of moderate and severe stunting (height-for-age) by age, sex and urban, rural and Indigenous area
* Change in stunting prevalence between the 2007 and 2013 censuses
* First-grade students who do not meet the age requirement
* Nutritional status of adults by health region

## Tools

* **First version (paper):** Python (web scraping, Tabula, pandas, GeoPandas) with a Plotly dashboard.
* **Current version:** R (`sf`, `dplyr`) and a Quarto dashboard with Observable JS, Leaflet and OpenStreetMap, published as a static site.
