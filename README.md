# US Income & Population Density Bivariate Map

This project visualizes the relationship between income and population density across the United States using a bivariate choropleth map. The map is created using Leaflet, a popular open-source JavaScript library for interactive maps.

## Project Overview

The project aims to provide a visual representation of how income and population density vary across different states in the US. By using a bivariate color scheme, the map allows users to easily identify areas with different combinations of income and population density.

## Files

- `index.html`: The main HTML file that contains the code for creating and displaying the map.
- `Income.js`: A JavaScript file containing income data for each state.
- `Density.js`: A JavaScript file containing population density data for each state.

## index.html

The `index.html` file is the core of the project. It includes the necessary HTML, CSS, and JavaScript to create and display the bivariate choropleth map.

### HTML Structure

The HTML structure includes the following key elements:

- A `<head>` section that includes the Leaflet CSS and custom styles for the map and legend.
- A `<body>` section that contains a `<div>` element with the ID `map`, which is where the map will be rendered.
- Script tags to include the Leaflet JavaScript library, `Income.js`, and `Density.js`.

### CSS Styles

The CSS styles define the appearance of the map and the legend:

- The `#map` element is styled to take up the full viewport.
- The `.legend` class styles the legend with a background, padding, shadow, and rounded corners.
- The `.legend-grid` class creates a grid layout for the legend cells.
- The `.legend-cell` class styles each cell in the legend grid.

### JavaScript Code

The JavaScript code initializes the map, processes the data, and adds the choropleth layer and legend.

#### Initializing the Map

```javascript
const map = L.map('map').setView([37.8, -96], 4);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
}).addTo(map);
