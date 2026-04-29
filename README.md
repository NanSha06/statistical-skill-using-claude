# mat-stats

A Claude skill for performing **statistical analysis, probability operations, and exploratory data analysis on MATLAB `.mat` files**.

## Overview

`mat-stats` helps load, inspect, summarize, visualize, and analyze data stored in MATLAB MAT files using Python libraries such as SciPy, NumPy, Pandas, Matplotlib, and h5py.

Use this skill whenever you need to:

* Analyze a `.mat` file
* Inspect variables inside MATLAB data files
  n- Compute descriptive statistics
* Run probability or distribution analysis
* Test correlations between variables
* Generate histograms and plots
* Work with legacy MAT files (`v4/v5`) or newer `v7.3` files

## Features

### File Loading

* Supports classic MAT formats via `scipy.io.loadmat`
* Supports MAT `v7.3` (HDF5-based) via `h5py`
* Automatically filters MATLAB metadata fields

### Data Inspection

* Detect variable names
  n- Show shapes, dtypes, dimensions
* Identify numeric vs non-numeric variables

### Statistical Analysis

* Mean, median, variance, standard deviation
* Percentiles and IQR
* Skewness and kurtosis
* Standard error of mean
* Summary reports

### Probability & Distributions

* Fit common distributions:

  * Normal
  * Exponential
  * Gamma
  * Weibull
  * Beta
  * Poisson
  * Binomial
* PDF / CDF / Quantile calculations
* Random sampling

### Hypothesis Testing

* One-sample t-test
* Two-sample t-test
* Paired t-test
* Mann-Whitney U
* Wilcoxon signed-rank
* ANOVA / Kruskal-Wallis
* Chi-square tests

### Correlation Analysis

* Pearson
* Spearman
* Kendall Tau
* Point-biserial

### Visualization

* Histograms
* Boxplots
* Scatter plots
* Distribution overlays

## Installation

```bash
pip install scipy numpy pandas matplotlib h5py
```

## Example Usage

```python
import scipy.io
nimport numpy as np

mat = scipy.io.loadmat('sample.mat')
print(mat.keys())
```

## Recommended Workflow

1. Load the `.mat` file
2. Inspect variables and shapes
3. Select numeric arrays
4. Run descriptive statistics
5. Test distributions / hypotheses
6. Visualize results
7. Export findings

## Included Reference

* `references/scipy_stats_cheatsheet.md`

  * Quick lookup for SciPy statistical functions
  * Hypothesis tests
  * Correlations
  * Confidence intervals
  * Distribution fitting

## Project Structure

```text
mat-stats/
├── SKILL.md
└── references/
    └── scipy_stats_cheatsheet.md
```

## Best Use Cases

* MATLAB dataset exploration
* Academic research data analysis
* Sensor signal statistics
* Simulation output validation
* Engineering experiments
* Machine learning preprocessing of MAT datasets

## Notes

* Flatten MATLAB row/column vectors before analysis.
* Check missing values before computing metrics.
* Use non-parametric tests when normality assumptions fail.
* Use `h5py` for MAT v7.3 files.

## License

Use freely for personal, research, and educational purposes.

## Author

Created as a Claude skill for advanced MAT file analytics.
