# Video Games Sales Insights

## Overview
This repository contains the cleaned datasets, notebooks, and Power BI assets
used to analyze global video game sales. It blends VGChartz exports with
marketing descriptors and clusters franchises by revenue, region, and platform
momentum.

## Repository Layout
- `Video_Game_Sales_Analysis_And_Clustering.ipynb` – the main notebook for
  feature engineering, clustering, and visualization.
- `Video Game Sales Data (Clean).csv` – curated dataset consumed by the Power BI
  dashboard.
- `vgsales.csv` – raw VGChartz export for reproducibility.
- `Video Game Sales Data - Analysis.pbix` / `.pdf` – interactive dashboards and
  static reports.
- `images/` – supporting figures for executive readouts.

## Environment Setup
1. Create a conda/virtual environment and install the data stack:
   ```powershell
   conda create -n vg-sales python=3.10 pandas numpy scikit-learn matplotlib seaborn jupyter
   conda activate vg-sales
   ```
2. Install Power BI Desktop (for editing `.pbix` files) if you need to refresh
   or publish visuals.

## Running Workflows
- Launch the notebook:
  ```powershell
  jupyter notebook "Video_Game_Sales_Analysis_And_Clustering.ipynb"
  ```
- Update the clean dataset by executing the ETL cells in the notebook and
  exporting to `Video Game Sales Data (Clean).csv`.
- Refresh the Power BI dashboard: open the `.pbix`, point it at the refreshed
  CSV, and publish/share as needed.

## Quality & Automation
- Keep CSVs under version control with LFS if they exceed GitHub’s size limits.
- Before pushing notebook changes, clear outputs (`jupyter nbconvert --clear-output`)
  to keep diffs manageable.
- When sharing results, export the dashboard to `.pdf` (already in repo) so
  stakeholders without Power BI can review the insights.
