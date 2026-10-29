# Electric Vehicle Market Performance & Insights

A responsive business-intelligence dashboard built with plain HTML, CSS and vanilla JavaScript. No frameworks, no backend, no build step.

## Important: data is synthetic

`data.csv` holds **40 synthetic sample records** with **fictional manufacturers and models**. The values were randomly generated for demonstration. They are **not real-world market statistics** and must not be cited as such. To analyse real data, replace `data.csv` with a verified dataset that uses the same columns.

## Features

- KPI cards: total records, average range, manufacturers, battery categories
- Charts: manufacturer, vehicle category (donut), model year, battery technology, range distribution
- Filters: manufacturer, model year, vehicle category, plus a reset button
- Data table with search across all columns and click-to-sort headers
- Responsive layout (desktop, tablet, mobile) with keyboard-focus styles
- KPIs and charts follow the filters. The table follows the filters and the search box.

## Project structure

```
ev-dashboard/
├── index.html   page structure
├── style.css    layout and theme
├── script.js    CSV loading, filters, charts, table
├── data.csv     synthetic sample data
└── README.md
```

## Data format

Columns: `id, manufacturer, model, year, category, battery_tech, battery_kwh, range_km`. Fields must not contain commas (the parser is intentionally simple).

## Run locally

Browsers block `fetch` on `file://` pages, so serve the folder:

```bash
cd ev-dashboard
python3 -m http.server 8000
```

Open http://localhost:8000.

## Deploy to GitHub Pages

1. Create a new **public** repository on github.com (for example `ev-dashboard`). Do not add a README there.
2. Upload the files, either way:
   - **Web:** on the empty repo page choose "uploading an existing file", drag in the five files (keep them at the repo root, not inside a subfolder), then click **Commit changes**.
   - **Command line**, from inside the project folder:
     ```bash
     git init
     git add .
     git commit -m "Add EV dashboard"
     git branch -M main
     git remote add origin https://github.com/<your-username>/ev-dashboard.git
     git push -u origin main
     ```
3. In the repo, open **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/ (root)**, then click **Save**.
6. Wait a minute or two, then refresh the Pages settings. The live URL appears at the top: `https://<your-username>.github.io/ev-dashboard/`.

If you see a 404, confirm that `index.html` is at the repository root and that the Pages source is set as above.

## License

Choose a license for your own use. The sample data is synthetic and free to modify.
