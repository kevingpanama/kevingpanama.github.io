---
title: "Structuring a Geospatial Information System for the Analysis of Food Security, Nutritional Intervention and Human Health Data in Panama"
original_title: "Estructuración de un sistema de información geoespacial para el análisis de datos de seguridad alimentaria, intervenciones nutricionales y de salud humana en Panamá"
language: "Spanish"
collection: publications
category: posters
permalink: /publication/2023-09-15-sistema-de-informacion-geoespacial-seguridad-alimentaria
excerpt: 'Building a geospatial information system for food security and nutrition data in Panama: web scraping and ETL turned Ministry of Health PDF reports into 96 geo-referenced indicators (2003–2014), mapped by province, and the basis of the PRISM nutrition layer.'
date: 2023-09-15
venue: 'XIX Congreso Nacional de Ciencia y Tecnología – APANAC 2023'
paperurl: '/files/gonzalez-ortega-2023-apanac-sistema-geoespacial.pdf'
citation: 'González Ortega, K., Aguilar, E., Aizprúa, A. G., Cedeño, E., &amp; Sánchez-Galán, J. (2023). &quot;Estructuración de un sistema de información geoespacial para el análisis de datos de seguridad alimentaria, intervenciones nutricionales y de salud humana en Panamá [Structuring a geospatial information system for the analysis of food security, nutritional intervention and human health data in Panama].&quot; <i>XIX Congreso Nacional de Ciencia y Tecnología – APANAC 2023</i>, pp. 356–362. https://doi.org/10.33412/apanac.2023.3959'
---

**Authors:** **Kevin González Ortega**, Eliecer Aguilar, Ana Gabriela Aizprúa, Eddy Cedeño, Javier Sánchez-Galán (Universidad Tecnológica de Panamá)<br/>
**Venue:** XIX Congreso Nacional de Ciencia y Tecnología – APANAC 2023, Panama, September 26–29, 2023, pp. 356–362 (ISSN 2805-1807)<br/>
**DOI:** [10.33412/apanac.2023.3959](https://doi.org/10.33412/apanac.2023.3959) · **[PDF](/files/gonzalez-ortega-2023-apanac-sistema-geoespacial.pdf)** (open access, CC BY-NC-SA 4.0)<br/>
**Keywords:** food security, web scraping, geo-referenced indicators, geographic information system, interdisciplinary spatial data analysis

**Language:** This paper is published in **Spanish**. The title above is an English translation.<br/>
**Original title:** *Estructuración de un sistema de información geoespacial para el análisis de datos de seguridad alimentaria, intervenciones nutricionales y de salud humana en Panamá*

## Summary

Few studies in Panama look at **food security** and its link to poverty, and there was no geospatial information system that showed where nutritional interventions had been carried out. Much of the relevant data existed only as **unstructured PDF reports** from the Nutrition Program of Panama's Ministry of Health (MINSA).

We built a reproducible pipeline that turns those reports into **96 geo-referenced indicators** of living standards, weight and height for 2003–2014, linked to the boundaries of Panama's provinces and *comarcas* and explored through interactive maps. The dataset is designed to become a layer of **[PRISM](/projects/prism/)** (Panama Research and Integrated Sustainability Model), where it can be analyzed alongside other layers such as water quality, biological connectivity and biodiversity.

## Methodology

1. **Web scraping.** We collected the nutritional-intervention reports published by MINSA's Nutrition Program.
2. **Table extraction.** We used **Tabula** to extract the indicator tables from the PDFs and export them as CSV.
3. **Consolidation.** We merged all extracted tables into one dataset with **pandas**.
4. **Geospatial processing.** We took province boundaries from an open GIS repository, added **ISO 3166-2** codes as a join key, and exported a **GeoJSON** file.
5. **Visualization.** We built an interactive **Plotly** dashboard with a selector for the nutrition indicators.

## Results

| Source document | Indicators |
|---|:---:|
| VI National Height Census of First-Grade Schoolchildren (2007): coverage, stunting by area, sex, age and school type, nutritional status | 45 |
| VII National Height Census (2013/2014): coverage, mean and median height at age 7, stunting by area and age, change 2007→2013 | 46 |
| Report on the Nutritional Situation of Population Groups in Panama (2016): nutritional status of adults by health region | 5 |
| **Total** | **96** |

The work shows that web scraping, OCR-based table extraction, data consolidation and interactive maps together give a full picture of nutritional indicators in Panama. That picture can support decisions in public health and nutrition.

**Related project:** [PRISM interactive dashboard](/projects/prism/), the current version of the map built from this data.

## BibTeX

```bibtex
@inproceedings{gonzalez2023estructuracion,
  title     = {Estructuraci{\'o}n de un sistema de informaci{\'o}n geoespacial para el an{\'a}lisis de datos de seguridad alimentaria, intervenciones nutricionales y de salud humana en Panam{\'a}},
  author    = {Gonz{\'a}lez Ortega, Kevin and Aguilar, Eliecer and Aizpr{\'u}a, Ana Gabriela and Cede{\~n}o, Eddy and S{\'a}nchez-Gal{\'a}n, Javier},
  booktitle = {XIX Congreso Nacional de Ciencia y Tecnolog{\'i}a -- APANAC 2023},
  pages     = {356--362},
  year      = {2023},
  address   = {Panam{\'a}},
  doi       = {10.33412/apanac.2023.3959}
}
```
