documentation/design/    Requirements and chart rationale
# The Roast Report: The Morning Rush

An interactive D3.js visualisation of coffee shop sales across Astoria, Hell's
Kitchen, and Lower Manhattan from January to June 2023. The project was
developed for the CIS4014 Interactive Visualisation coursework by Group 4.

## Live Dashboard

[Open The Roast Report](https://inkymello.github.io/The-Roast-Report---The-Morning-Rush/)

The dashboard is a static web application published through GitHub Pages. No
installation is required to use the published version.

## Project Aim

The dashboard makes the sales data easier to explore by showing:

- when transactions take place;
- where revenue comes from across the three stores;
- how daily revenue relates to units sold; and
- how the selected store, category, and month change the results.

The design combines summary metrics with coordinated charts so users can move
from a high-level view to detailed comparisons without leaving the page.

## Dataset

The cleaned transaction table covers January to June 2023 and contains:

| Measure | Value |
| --- | ---: |
| Transaction rows | 149,116 |
| Units sold | 214,470 |
| Revenue | $698,812.33 |
| Stores | Astoria, Hell's Kitchen, Lower Manhattan |

The source and cleaned workbooks are stored in [`data/`](data/). The web
application performs filtering and aggregation in the browser.

## Dashboard Features

### KPI summaries

The dashboard displays revenue, transaction count, units sold, average
transaction value, and the busiest hour for the current selection.

### When: transaction heat map

A day-of-week and hour-of-day heat map shows when transaction activity is
highest. Hovering over a cell reveals its details, and clicking can hold the
hour selection.

### Where: store map and ranking

A simplified map shows the three store locations, with circle size based on
revenue. The linked ranking shows each store's position, revenue spread, and
units per transaction. Selecting a store from either view filters the page.

### How much: daily revenue scatter plot

A scatter plot compares daily revenue with daily units sold. Point size
represents the number of transactions for the store-day. The analysis panel
reports the regression equation, R-squared, correlation, revenue per extra
unit, and number of store-days plotted.

## Interactions

- Filter by store, product category, or month.
- Clear all filters with the reset control.
- Hover over heat-map cells and store marks for additional detail.
- Select a store on the map or in the ranking to filter all views.
- Drag across the scatter plot to zoom into a range of values.
- Reset the scatter-plot zoom after exploring a subset.
- Use the section links to move between the When, Where, and How much views.

All visualisations and KPI summaries update together when a filter changes.

## Technology

- HTML5 for page structure and accessible chart labels
- CSS3 for responsive layout, typography, colour, and chart styling
- JavaScript for filtering, aggregation, regression calculations, and events
- D3.js v7 for SVG charts, scales, axes, transitions, and map geometry
- GitHub Pages for static hosting
- jsDelivr CDN for the D3.js dependency
- Google Fonts for the dashboard typography

## Run Locally

The application has no build step, package manager, or server-side code.

### Option 1: Open the page directly

Open [`web/index.html`](web/index.html) in a modern browser. An internet
connection is required for D3.js v7 and the Google Fonts loaded from CDNs.

### Option 2: Use a local static server

From the repository root, run:

```text
python -m http.server 8000
```

Then open <http://localhost:8000/web/>.

## Web Application Files

| File | Purpose |
| --- | --- |
| [`web/index.html`](web/index.html) | Page structure, controls, chart containers, and external dependencies. |
| [`web/js/script.js`](web/js/script.js) | Embedded data, filtering, aggregation, chart drawing, and interactions. |
| [`web/css/style.css`](web/css/style.css) | Responsive layout, typography, colours, and visual styling. |
| [`web/README.md`](web/README.md) | Web application-specific usage and feature notes. |

## Repository Contents

| Location | Purpose |
| --- | --- |
| [`data/`](data/) | Raw and cleaned coffee shop sales datasets. |
| [`charts/`](charts/) | Individual chart work organised by group member. |
| [`prototypes/`](prototypes/) | Early heat-map, store-map, and scatter-plot explorations. |
| [`dashboard/initial dashbaord/`](dashboard/initial%20dashbaord/) | Earlier dashboard implementation retained as project history. |
| [`documentation/data cleaning/`](documentation/data%20cleaning/) | Data preparation records. |
| [`documentation/design/`](documentation/design/) | Design requirements, rationale, UI design, and interaction evidence. |
| [`documentation/meetings/`](documentation/meetings/) | Sprint and final team meeting records. |
| [`documentation/scrum/`](documentation/scrum/) | Product backlog, sprint backlogs, burndown charts, and retrospectives. |
| [`documentation/testing/`](documentation/testing/) | Testing and bug-fixing evidence. |

See [`README_STRUCTURE.md`](README_STRUCTURE.md) for the current file and
directory inventory.

## Documentation

- [Final Documentation](documentation/FINAL_DOCUMENTATION.md) - consolidated
  project summary, methodology, features, testing, and limitations.
- [GitHub Documentation](documentation/GITHUB_DOCUMENTATION.md) - repository
  usage, local setup, deployment, and contribution workflow.
- [Final Team Review](documentation/meetings/Final_Team_Review.docx)
- [Final Scrum Review](documentation/scrum/Final_Scrum_Review.docx)
- [Design documentation](documentation/design/)
- [Data-cleaning documentation](documentation/data%20cleaning/)
- [Testing documentation](documentation/testing/)

## Testing and Quality Checks

The final review covered:

- loading the dashboard and external D3 dependency;
- initial KPI and chart rendering;
- store, category, and month filters;
- clearing filters and releasing a selected store;
- heat-map and store-map interaction;
- scatter-plot zoom and reset controls;
- responsive layout at narrower viewport widths; and
- repository links and documentation structure.

Detailed evidence is available in the [testing documentation](documentation/testing/)
and [Final Team Review](documentation/meetings/Final_Team_Review.docx).

## Known Limitations

- The dashboard depends on CDN-hosted D3.js and fonts when opened online.
- The analysis covers only the supplied January to June 2023 dataset.
- The store map uses simplified geometry rather than a live map or tile service.
- The application is client-side only and has no persistent user state or API.

## Project Status

The final interactive visualisation and supporting coursework documentation are
available in this repository. The `dashboard/initial dashbaord/` directory and
the prototype files are retained to show the development process.
