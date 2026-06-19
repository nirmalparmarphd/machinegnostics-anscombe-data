# Machine Gnostics Tutorial Series with Anscombe Quartet

This folder is organized as a full step-by-step learning path for users who are new to Machine Gnostics.

Important note:
- `anscombe_data.ipynb` is your high-level notebook and is intentionally left unchanged.

## Tutorial Path
Run the notebooks in this order:

1. `part_0_setup.ipynb`
2. `part_1_gnostic_metrics.ipynb`
3. `part_2_gnostic_distribution_functions.ipynb`
4. `part_3_gnostic_marginal_interval_analysis.ipynb`
5. `part_4_gnostic_linear_regression.ipynb`

## What Each Notebook Teaches

### Part 0 - Setup and Orientation
- install dependencies
- import Machine Gnostics and classical stack
- load Anscombe data and verify basics

### Part 1 - Gnostic Metrics
- mean, median, correlation
- R2, robust R2, RMSE comparisons
- side-by-side table: NumPy/Sklearn vs Machinegnostics

### Part 2 - Distribution Functions
- EGDF and ELDF concepts
- ELDF vs empirical CDF + KDE PDF
- final presentation plot saved as:
  - `eldf_vs_cdf_pdf_y_2x4.png`

### Part 3 - Marginal Interval Analysis
- classical 95% confidence interval for mean
- Machine Gnostics typical/tolerance intervals
- 2x2 cross-dataset interval comparison

### Part 4 - Linear Regression Poster
- sklearn linear regression vs Machine Gnostics linear regression
- mean/median markers and per-dataset metrics tables
- final poster saved as:
  - `anscombe_quartet_poster.png`

## Google Colab Links
Open notebooks directly in Google Colab:

| Notebook | Topic | Colab Link |
|----------|-------|-----------|
| Part 0 | Setup and Orientation | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/part_0_setup.ipynb) |
| Part 1 | Gnostic Metrics | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/part_1_gnostic_metrics.ipynb) |
| Part 2 | Distribution Functions | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/part_2_gnostic_distribution_functions.ipynb) |
| Part 3 | Interval Analysis | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/part_3_gnostic_marginal_interval_analysis.ipynb) |
| Part 4 | Linear Regression | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/part_4_gnostic_linear_regression.ipynb) |
| Quick Study | End-to-end reference notebook | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nirmalparmarphd/machinegnostics-anscombe-data/blob/main/anscombe_data.ipynb) |

## Local Setup

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -U pip
pip install machinegnostics numpy pandas matplotlib seaborn scipy scikit-learn jupyter
```

# Machine Gnostics Documentations
Documentation available at: https://docs.machinegnostics.com/latest/