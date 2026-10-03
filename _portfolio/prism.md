---
title: "PRISM: Panama Research and Integrated Sustainability Model"
excerpt: "Interactive geospatial dashboard mapping child stunting and school-age indicators across Panama's provinces, built with R, Quarto and Leaflet. Universidad Tecnológica de Panamá.<br/>[Open the dashboard](/PRISM/dashboard.html)"
collection: portfolio
order: 1
---

**Team:** K. González, E. Aguilar, A. G. Aizprúa, E. Cedeño, J. E. Sánchez-Galán — Universidad Tecnológica de Panamá

**[Open the interactive dashboard →](/PRISM/dashboard.html)** · [Source code](https://github.com/kevingpanama/kevingpanama.github.io/tree/main/PRISM)

PRISM is an interactive geospatial dashboard that maps province-level indicators from Panama's school height census of children aged 6–9. Users pick one of 50+ indicators from a menu and the choropleth map recolors each province, with tooltips showing the value for each.

The indicators include:

* Census coverage of schoolchildren aged 6–9
* Median and mean height of 7-year-old boys and girls
* Prevalence of moderate and severe stunting (height-for-age), by age and by urban, rural and Indigenous areas
* Change in stunting prevalence between the 2007 and 2013 censuses
* First-grade students who do not meet the age requirement

**Methods and tools:** R (`sf`, `dplyr`) to join census tables to provincial boundaries (ISO 3166-2), and a Quarto dashboard using Observable JS and Leaflet with a viridis color scale.
