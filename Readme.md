# Diamond Price Prediction Notebook

A Jupyter Notebook demonstrating an end-to-end workflow to predict diamond prices using the classic "diamonds" dataset.

This repository contains:
- `diamonds.ipynb` — Jupyter notebook with Exploratory Data Analysis (EDA), preprocessing, feature engineering, model training and evaluation.
- `data/diamonds.csv` — dataset used by the notebook (expected path: `./data/diamonds.csv`).

## Quick summary
- Task: Predict the price of a diamond from features such as `carat`, `cut`, `color`, `clarity`, `depth`, `table`, and dimensions (`x`, `y`, `z`).
- Dataset size (as used in the notebook): 53,940 rows × 10 columns.
- Notable EDA observations:
  - No missing values reported.
  - Some `x`, `y`, `z` values are zero — likely invalid measurements that should be handled in preprocessing.
  - `price` distribution is right-skewed; consider log-transforming the target for modeling.
  - The dataset contains both numerical and categorical features (`cut`, `color`, `clarity`).

## How to run locally

1. Clone the repository
   ```bash
   git clone https://github.com/pinsdev24/diamond-price-prediction-notebook.git
   cd diamond-price-prediction-notebook
   ```

2. (Optional but recommended) Create and activate a Python virtual environment
   ```bash
   python -m venv .venv
   source .venv/bin/activate      # macOS / Linux
   .\.venv\Scripts\activate       # Windows (PowerShell/CMD)
   ```
3. Start Jupyter and open the notebook
   ```bash
   jupyter notebook diamonds.ipynb
   ```
   or
   ```bash
   jupyter lab
   ```

## Notebook overview

The notebook walks through:
- EDA: dataset shape, datatypes, value counts, descriptive statistics, and visualizations (histograms, pairplots, grouped summaries).
- Data cleaning and preprocessing: handling invalid dimensions (`x`, `y`, `z`), encoding categorical variables, optional scaling, and target transformation suggestions.
- Modeling: train/test split, baseline models, more advanced regressors (example: tree-based models), training, and evaluation with regression metrics (RMSE).
- Feature analysis: group summaries, feature importance from tree-based models.

## License & contact
- License: MIT (adjust if needed)
- Author: pinsdev24 — open an issue or PR for questions, suggestions, or improvements.
