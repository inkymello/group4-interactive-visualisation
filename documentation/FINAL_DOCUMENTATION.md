# Final Documentation

## Project Overview

The Roast Report is an interactive D3.js visualisation of coffee shop sales
from January to June 2023. It examines when transactions occur, where revenue
comes from, and how daily revenue relates to units sold across Astoria, Hell's
Kitchen, and Lower Manhattan.

The final dashboard is available at:

<https://inkymello.github.io/The-Roast-Report---The-Morning-Rush/>

## Objectives

The project was designed to make the sales dataset easier to explore through:

- clear summaries of revenue, transactions, units sold, average transaction
  value, and busiest hour;
- coordinated filtering by store, product category, and month;
- views that support temporal, geographic, and relationship-based analysis; and
- direct interaction with chart marks to reveal more detailed values.

## Data Summary

The cleaned transaction table contains 149,116 rows, 214,470 units, and
$698,812.33 in revenue across the six-month period. The web application uses
the cleaned transaction data and performs filtering and aggregation in the
browser.

## Final Visualisations

### When

A day-of-week and hour heat map shows when transaction activity is highest.
Hovering reveals hourly details and clicking can hold an hour selection.

### Where

A simplified map places the three stores geographically and sizes the store
marks by revenue. A linked ranking provides a second way to select a store and
shows the revenue spread and units per transaction.

### How much

A scatter plot compares daily revenue with daily units sold. Point size
represents transaction count, while the summary reports the regression
equation, R-squared, correlation, revenue per extra unit, and number of
store-days plotted.

## Interaction Design

Store, category, and month controls update the KPI summaries and all chart
views together. Store marks and ranking entries can be selected directly. The
scatter plot supports drag-to-zoom and provides a reset control after zooming.
The layout is responsive so the dashboard remains usable on smaller screens.

## Technology

- HTML5 for document structure
- CSS3 for responsive layout and visual styling
- JavaScript for filtering, aggregation, and interaction logic
- D3.js v7 for scales, SVG charts, axes, map geometry, and transitions
- GitHub Pages for static hosting

## Testing and Quality Checks

The final review included checks of the dashboard in a modern browser, with
attention to:

- loading the page and its external D3 dependency;
- displaying the initial KPI and chart states;
- applying each filter and clearing filters;
- selecting and releasing a store from the map and ranking;
- using scatter-plot zoom and reset controls;
- checking responsive layout at narrower viewport widths; and
- checking the repository links and documentation structure.

Detailed project evidence is available in the [testing documentation](testing/)
and the [Final Team Review](meetings/Final_Team_Review.docx).

## Known Limitations

- The dashboard depends on CDN-hosted D3.js and fonts when opened online.
- The visualisation covers the supplied January to June 2023 dataset only.
- The map is simplified geometry rather than a live geographic map or tile
  service.
- The application is a static client-side page and does not provide a server
  API or persistent user state.

## Supporting Records

- [GitHub Documentation](GITHUB_DOCUMENTATION.md)
- [Final Team Review](meetings/Final_Team_Review.docx)
- [Final Scrum Review](scrum/Final_Scrum_Review.docx)
- [Design documentation](design/)
- [Data-cleaning documentation](data%20cleaning/)
- [Testing documentation](testing/)