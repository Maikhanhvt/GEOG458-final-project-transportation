# Walking Accessibility to Transportation in Seattle

GEOG 458 Group 17

## AI Disclosure
No AI tools are used in this project.

## Project URL

- Project site: [https://maikhanhvt.github.io/GEOG458-final-project-transportation/](https://maikhanhvt.github.io/GEOG458-final-project-transportation/)
- Main dashboard: [https://maikhanhvt.github.io/GEOG458-final-project-transportation/map.html](https://maikhanhvt.github.io/GEOG458-final-project-transportation/map.html)

## Team Members

- Maikhanh Tran
- Martin Yuan
- Lindsay Nguyen
- Samir Deo

## Project Description

This project is an interactive web dashboard that visualizes public transportation accessibility across Seattle. It combines neighborhood boundaries, transit stops, and transit routes so users can compare how transit service varies between different parts of the city.

The project is designed for students, elders, commuters, transit-dependent residents, and people who do not have access to a private vehicle. Its purpose is to provide a clear and intuitive way to understand how public transportation connects Seattle neighborhoods and where access appears stronger or more limited.

## Screenshots

The following screenshots show the current webpages included in this project repository.

![Seattle transportation map dashboard](assets/screenshot%201.png)

![User guide page](assets/screenshot%202.png)

![About page](assets/screenshot%203.png)

## Project Goal

The main message of this project is that walk-based access to public transportation is not evenly distributed across Seattle neighborhoods. By allowing users to compare transit stops, route coverage, and a neighborhood accessibility index, the dashboard helps reveal which areas are better served by transit and which areas may be underserved.

## Main Functions

- Zoom to a Seattle neighborhood from a dropdown menu.
- View the number of transit stops in the current map extent or in a selected neighborhood.
- Compare transit stop distribution by direction using a dynamic bar chart.
- Toggle transit routes, transit stops, and neighborhood boundaries on and off.
- Click transit stops and route lines to open popups with more information.
- Compute a Neighborhood Accessibility Index for the selected neighborhood.
- Reset the dashboard and return to the default Seattle-wide view.

## How Accessibility Is Represented

The current implementation represents neighborhood accessibility with a simple comparative indicator: the number of in-service transit stops inside the selected neighborhood divided by neighborhood area in square kilometers. This accessibility index is intended to support neighborhood comparison within the dashboard.

## Data Sources

1. **TRANSITSTOP_POINT**  
   King County Open Data. Point layer of public transit stop locations across King County and Seattle.  
   Source: [https://www5.kingcounty.gov/sdc?Layer=TRANSITSTOP_POINT](https://www5.kingcounty.gov/sdc?Layer=TRANSITSTOP_POINT)

2. **TRANSITROUTE_LINE / King County Metro Routes**  
   King County Open Data. Line layer of transit routes with route identifiers and service information.  
   Source: [https://gis-kingcounty.opendata.arcgis.com/datasets/kingcounty::king-county-metro-routes/explore?location=47.387823%2C-122.098240%2C8](https://gis-kingcounty.opendata.arcgis.com/datasets/kingcounty::king-county-metro-routes/explore?location=47.387823%2C-122.098240%2C8)

3. **Neighborhood Map Atlas Neighborhoods**  
   Seattle Open Data. Polygon layer defining Seattle neighborhood boundaries.  
   Source: [https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::neighborhood-map-atlas-neighborhoods/explore?location=47.614610%2C-122.336918%2C10](https://data-seattlecitygis.opendata.arcgis.com/datasets/SeattleCityGIS::neighborhood-map-atlas-neighborhoods/explore?location=47.614610%2C-122.336918%2C10)

4. **Spatial joined GeoJSON layers**  
   The repository also includes joined layers such as `stop-joined-neig.geojson` and `route-joined-neig.geojson`, which support visualization and neighborhood-level summary analysis in the dashboard.

## Applied Libraries and Web Services

- **MapLibre GL JS** for interactive web mapping.
- **Turf.js** for spatial analysis such as point-in-polygon tests, area calculation, and bounding boxes.
- **D3.js** and **C3.js** for the dynamic summary chart.
- **GitHub** and **GitHub Pages** for code hosting and project publishing.
- **CARTO basemap tiles** with **OpenStreetMap** attribution for the base map.
- **King County Open Data** and **Seattle Open Data / ArcGIS Online** for public transit and neighborhood datasets.

## Other Information

- The project currently includes three main pages: `map.html`, `guide.html`, and `about.html`.
- The map interface accommodates color-blind users.
- The map highlights in-service transit stops, transit routes, neighborhood boundaries, and an accessibility summary that users can interpret alongside the chart and popups.

## Acknowledgment

- GEOG 458 course materials and Lab 6 for the dashboard mapping workflow that inspired this project structure.
- Project inspiration from the [WSDOT Real-time Map](https://wsdot.com/Travel/Real-time/Map/) and [OneBusAway](https://onebusaway.org/).
- King County Metro, King County Open Data, and Seattle Open Data for the transit and neighborhood datasets used in this project.
- CARTO and OpenStreetMap for basemap support.
