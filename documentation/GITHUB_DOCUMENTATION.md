# GitHub Documentation

## Repository

This repository contains the CIS4014 Group 4 interactive visualisation project,
including the source data, cleaned data, exploratory chart work, design
records, Scrum evidence, testing records, and final web application.

The public repository is:

<https://github.com/inkymello/group4-interactive-visualisation>

The published dashboard is:

<https://inkymello.github.io/The-Roast-Report---The-Morning-Rush/>

## Repository Layout

| Location | Contents |
| --- | --- |
| `data/` | Raw and cleaned coffee shop sales datasets. |
| `charts/` | Individual chart work by group member. |
| `prototypes/` | Early chart and interface explorations. |
| `documentation/` | Design, data cleaning, meeting, Scrum, testing, and final records. |
| `web/` | The deployable static dashboard. |

## Run the Dashboard Locally

The dashboard has no build process or server-side dependencies.

1. Clone the repository.
2. Open `web/index.html` in a current browser, or serve the repository with a
   local static file server.
3. Keep an internet connection available because D3.js v7 and the interface
   fonts are loaded from CDNs.

For example, from the repository root:

```text
python -m http.server 8000
```

Then open `http://localhost:8000/web/`.

## Git Workflow

Use a feature branch for changes and keep commits focused. Before opening a
pull request:

- check that links and documentation paths work;
- open the dashboard at desktop and mobile widths;
- verify that the filters update all visualisations together;
- check the browser console for errors; and
- describe the change and validation performed in the pull request.

Do not commit generated editor files, credentials, or unrelated personal data.

## GitHub Pages

The published site is a static deployment of the `web/` directory. When the
dashboard changes, confirm that the relative references to `css/style.css` and
`js/script.js` still resolve and that the deployment continues to load the D3
CDN dependency.

## Documentation Map

- [Final Documentation](FINAL_DOCUMENTATION.md)
- [Design documentation](design/)
- [Data-cleaning documentation](data%20cleaning/)
- [Testing documentation](testing/)
- [Scrum records](scrum/)
- [Meeting records](meetings/)