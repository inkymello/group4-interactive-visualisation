# The Roast Report: The Morning Rush

An interactive D3.js visualization exploring coffee shop sales across Astoria, Hell's Kitchen, and Lower Manhattan from January to June 2023.

**Live visualization:** https://inkymello.github.io/The-Roast-Report---The-Morning-Rush/

## Live visualization

[Open The Roast Report](https://inkymello.github.io/The-Roast-Report---The-Morning-Rush/)

The link opens the published interactive visualization directly in a web browser. No installation is required.

## What it shows

- When transactions happen, using a day-and-hour heat map.
- Where revenue comes from, using a store map and ranking.
- How daily revenue relates to units sold, using a scatter plot and regression summary.
- Revenue, transactions, units sold, average transaction value, and the busiest hour through responsive KPI summaries.

## Interactions

Use the store, category, and month filters to update every view together. Heat-map cells and store markers provide additional details on hover, while clicking a store filters the analysis. The scatter plot supports drag-to-zoom, with a reset control available after zooming.

## Run locally

This is a static web page with no build step or server-side code.

1. Open `index.html` in a modern browser.
2. Keep an internet connection available so the page can load D3.js v7 and the Google Fonts used by the interface.

Alternatively, serve the folder with any static web server and open the supplied local URL.

## Project files

- `index.html` - page structure and D3.js entry points.
- `js/script.js` - embedded dataset, filtering, aggregation, and chart interactions.
- `css/style.css` - responsive layout, typography, colors, and chart styling.

## Dataset summary

The cleaned transaction table contains 149,116 rows, 214,470 units, and $698,812.33 in revenue across the six-month period.

## Technologies

- HTML5
- CSS3
- JavaScript
- D3.js v7 via jsDelivr CDN