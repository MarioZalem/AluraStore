# Copilot Instructions for AluraStoreLatam

## Project Overview

This project is a data analysis challenge focused on retail store data for the "AluraStoreLatam". The workspace consists of a Jupyter notebook (`AluraStoreLatam.ipynb`) and a directory of CSV files containing store data (`base-de-datos-challenge1-latam/`).

## Data Structure

- All raw data is stored in CSV files under `base-de-datos-challenge1-latam/` (e.g., `tienda_1 .csv`, `tienda_2.csv`, etc.).
- The notebook loads these files directly from local disk or from remote URLs for reproducibility.

## Notebook Workflow

- The main workflow is in `AluraStoreLatam.ipynb`, organized by analysis sections:
  1. Importación de datos (Data Import)
  2. Análisis de facturación (Billing Analysis)
  3. Ventas por categoría (Sales by Category)
  4. Calificación promedio de la tienda (Average Store Rating)
  5. Productos más y menos vendidos (Most/Least Sold Products)
  6. Envío promedio por tienda (Average Shipping per Store)
- Each section typically contains a markdown cell for context and one or more code cells for analysis.

## Conventions & Patterns

- Use `pandas` for all data manipulation and analysis.
- Data is loaded into separate DataFrames for each store (e.g., `tienda`, `tienda2`, ...).
- When combining data, use `pd.concat` or `pd.merge` as appropriate.
- Visualizations (if added) should use `matplotlib` or `seaborn` for consistency.
- All code and outputs should be reproducible from a clean kernel restart.

## Developer Workflows

- No build or test scripts are present; all work is performed interactively in the notebook.
- To add new analyses, create a new markdown cell for the section header and context, followed by code cells.
- To update data, replace or add new CSV files in `base-de-datos-challenge1-latam/` and update the notebook import paths if needed.

## Integration Points

- The notebook can load data from both local files and remote URLs (see the import section for examples).
- No external APIs or services are integrated beyond data file access.

## Examples

- To load a new store's data:
  ```python
  tienda5 = pd.read_csv('base-de-datos-challenge1-latam/tienda_5.csv')
  ```
- To concatenate all stores:
  ```python
  all_tiendas = pd.concat([tienda, tienda2, tienda3, tienda4], ignore_index=True)
  ```

## Key Files & Directories

- `AluraStoreLatam.ipynb`: Main analysis notebook
- `base-de-datos-challenge1-latam/`: Directory containing all raw CSV data files

## Additional Notes

- File naming in `base-de-datos-challenge1-latam/` may contain spaces; handle paths carefully.
- Keep notebook sections clearly separated and documented for readability.

---

_Last updated: July 2025_
