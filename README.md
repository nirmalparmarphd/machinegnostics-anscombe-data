# [Machine Gnostics](https://www.machinegnostics.info/latest/) GDF Tutorial — Anscombe's Quartet

This folder contains a step-by-step Jupyter notebook that introduces Machinegnostics Gnostic Distribution Functions (GDF) using Anscombe’s Quartet. It guides learners through concepts, visual comparisons, summary metrics, and side-by-side linear regression (sklearn vs Machinegnostics).

## What You’ll Learn
- GDF classes and selection axes: EGDF, ELDF, QGDF, QLDF via Estimating vs Quantifying and Local vs Global.
- How ELDF differs from classical empirical CDF and KDE/Histogram PDF.
- How to compute and interpret mean, median, and correlation using NumPy vs Machinegnostics.
- How to compare sklearn `LinearRegression` to Machinegnostics `LinearRegressor` with R², RMSE, and correlation.

## Folder Contents
- `anscombe_data.ipynb`: The main tutorial notebook.
- Generated images (after running the notebook):
  - `eldf_vs_cdf_pdf_y_2x4.png`: ELDF vs Empirical CDF and KDE/Histogram PDF (varS False/True).
  - `anscombe_quartet_poster.png`: Regression plots + per-dataset metrics tables.

## Prerequisites
- Python 3.9+
- Jupyter (or VS Code with Python + Jupyter extensions)
- Packages: `machinegnostics`, `numpy`, `matplotlib`, `seaborn`, `pandas`, `scikit-learn`

Install minimal dependencies in a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -U pip
pip install machinegnostics numpy matplotlib seaborn pandas scikit-learn jupyter
```

## Quick Start
1. Open the notebook `anscombe_data.ipynb`.
2. Run cells in order, following the step headers:
   - Step 1 — Setup & Data Loading
   - Step 2 — Learn GDF Concepts
   - Step 3 — ELDF vs Empirical CDF & KDE PDF (varS toggle)
   - Step 4 — Stats & Correlation (NumPy vs Machinegnostics)
   - Step 5 — Regression Prep (DataFrame)
   - Step 6 — Regression Comparison (sklearn vs Machinegnostics)
   - Step 7 — Wrap-up & Next Steps
3. Inspect the generated images and tables.

## Tutorial Flow (Highlights)
- **ELDF vs CDF/PDF:** ELDF (blue) smooths the empirical CDF (green) and offers a model-derived PDF (orange). Compare it with KDE (red), noting bandwidth sensitivity. Use `varS=True` to reveal heteroscedastic spread.
- **Stats & Correlation:** Per-dataset means/medians for x and y, plus correlation (NumPy vs Machinegnostics) printed and summarized in a DataFrame.
- **Regression Comparison:** Scatter plots for datasets I–IV, fitted lines for sklearn and Machinegnostics, and per-dataset metrics tables (R², RMSE, Corr, mean/median).

## Interpreting Results
- **Choosing a GDF:**
  - EGDF (E/G): Central truth + bounds; robust to outliers.
  - ELDF (E/L): Cluster/interval structure; dampens outliers.
  - QGDF (Q/G): Global anomaly emphasis.
  - QLDF (Q/L): Peripheral detail emphasis.
- **ELDF Benefits:** Assumption-free, robust smoothing; avoids bin/bandwidth pitfalls of hist/KDE; supports `varS` for heteroscedastic cases.
- **Regression & Metrics:** Machinegnostics regressors and metrics complement classical tools, often providing robustness in small, noisy samples.

## Saving Outputs
- Stats table: after running, save with `comparison_df.to_csv('anscombe_stats_comparison.csv')`.
- Figures are saved automatically by the plotting cells to PNG files in this folder.

## References
- ELDF documentation: https://www.machinegnostics.info/v0.0/da/eldf/
- Machinegnostics project: https://github.com/MachineGnostics/machinegnostics

## Next Steps
- Try EGDF/QGDF/QLDF on the same data to see axis effects.
- Use weights and bounds to encode domain knowledge.
- Apply the pipeline to your own datasets and compare classical vs gnostic outcomes.
