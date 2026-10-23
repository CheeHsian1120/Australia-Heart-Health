# Australia Heart Health

![Vega-Lite](https://img.shields.io/badge/Vega--Lite-BC63F8?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)

A comprehensive, interactive web-based data visualisation dashboard exploring the historical trends, geographical distribution, and socioeconomic impacts of Cardiovascular Disease in Australia. 

🌐 **[Live Demo](https://cheehsian1120.github.io/Australia-Heart-Health/)**

## 📊 Project Overview

This project transforms decades of complex health data from the Australian Bureau of Statistics (ABS) and the Australian Institute of Health and Welfare (AIHW) into an accessible, narrative-driven dashboard. The project is divided into three core storytelling segments:
1. **National Trends:** Historical mortality and hospitalisation rates.
2. **The People and Places:** Geographical hotspots and demographic disparities.
3. **Risks & Costs:** Lifestyle risk factors, pharmaceutical dependency, and economic burden.

## 🛠️ Technical Architecture

This project is built using a lightweight, static frontend stack, relying on declarative grammar for data visualisation.

* **Vega-Lite & Vega-Embed:** Used as the primary data visualisation grammar. Charts are defined purely in **JSON** specifications, allowing for rapid iteration, responsive scaling, and declarative interactive bindings (e.g., parameter dropdowns).
* **TopoJSON:** Utilised for all geographical map idioms. By using TopoJSON over standard GeoJSON, the spatial data footprint is significantly reduced, ensuring fast load times while maintaining high-fidelity boundary data for Australian States and Local Government Areas (LGAs).
* **HTML5 & CSS3:** Semantic HTML structure paired with custom CSS. Features include CSS Grid/Flexbox for side-by-side storytelling layouts, absolute positioning for contextual annotations, and custom typography to establish visual hierarchy.
* **Vanilla JavaScript:** Handles DOM manipulation outside of Vega's internal state, such as custom map toggles (State vs. Shire), dynamic text insight updates, and an `IntersectionObserver` for smooth, scroll-triggered fade-in animations.

## 🎨 Data Visualisation Principles Applied

The dashboard was strictly designed adhering to core data visualisation and UI/UX principles:

* **High Data-Ink Ratio:** Minimalist chart design. Gridlines are muted or removed, axes are simplified, and borders are eliminated to ensure the data itself stands out.
* **Color Theory & Semantics:** 
  * A carefully selected, muted earth-tone palette reduces eye strain. 
  * **Semantic mapping:** A distinct deep red (`#8c1527`) is consistently used to highlight danger, mortality, and peak cardiovascular burden across different charts, providing a cohesive visual language.
* **Storytelling & Annotation:** Absolute positioned HTML text elements are overlaid on Vega-Lite charts to provide immediate contextual insights, guiding the user's eye to key takeaways (e.g., pointing out the obesity threshold on the Ridgeline plot).
* **Geospatial Mapping Idioms:** 
  * **Choropleth Maps:** Used to show Age-Standardised Rates (ASR) to account for population density variations.
  * **Proportional Symbol Maps:** Used to show the raw, absolute volume of hospital admissions, highlighting logistical infrastructure strain in eastern seaboard cities.
  * **Hexagonal Cartogram:** Used to normalise geographical size distortions, representing equal population distribution (1 Hexagon = 250,000 Adults) when displaying lifestyle risks.
* **Advanced Chart Idioms:** Implementation of Streamgraphs, Diverging Bar Charts (Population Pyramid), Ridgeline Plots, Lollipop Charts, Dumbbell Plots, and Waterfall Charts to best fit the dimensionality and nature of specific datasets.

## 📁 Repository Structure

```text
├── index.html          # Main HTML document and layout
├── css/
│   └── style.css       # Styling, layout, and animation definitions
├── json/               # Vega-Lite JSON specifications and TopoJSON files
│   ├── streamgraph.json
│   ├── hBarChart.json
│   ├── divergingBarChart.json
│   ├── heatmap.json
│   ├── stateMap.json
│   ├── choroplethMap.json
│   ├── symbolMap.json
│   ├── hexCarto.json
│   ├── ridgeLine.json
│   ├── lollipop.json
│   ├── dumbbell.json
│   └── waterfall.json
├── data/               # Dataset
└── README.md
```

## ✍️ Author

Tay Chee Hsian