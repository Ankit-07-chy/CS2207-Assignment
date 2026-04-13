# CS2207 Group Project

## Anomaly Detection in Credit Card Usage

This repository contains the group project for CS2207: Anomaly Detection in Credit Card Usage. The goal is to analyze credit card transaction behavior, cluster cardholders using DBSCAN, and identify outlier usage patterns that may indicate anomalous or unusual customer behavior.

---

## Project Objective

Use Density-Based Spatial Clustering of Applications with Noise (DBSCAN) to find clusters in high-dimensional credit card usage data and detect noise points as potential anomalies.

Key tasks:
- Perform exploratory data analysis on credit card usage metrics such as balances, purchase amounts, and transaction frequency.
- Clean and normalize the dataset, handling missing values and scaling features.
- Apply DBSCAN clustering and tune parameters using a k-distance plot.
- Test multiple `MinPts` values to identify robust clustering behavior.
- Profile the data points classified as noise and interpret them as outliers.

---

## Repository Structure

- `README.md` - Project overview and usage instructions.
- `pyproject.toml` - Project metadata and Python requirements.
- `code/experiments/` - Experimental analysis files, notebooks, and exploratory scripts.
- `code/finalized/` - Final implementation, cleaned scripts, and report-ready code.
- `data/` - Dataset files used for analysis.
- `requirements.txt` - Used Libraries with Version.

---

## Dataset

The assignment uses a credit card dataset for clustering analysis. The dataset should contain customer transaction and usage metrics appropriate for density-based clustering. Place the dataset files in the `data/` folder before running the analysis.

> If you have the dataset downloaded separately, rename it consistently (for example `data/credit_card_usage.csv`).

---

## Getting Started

### Requirements

- Python 3.13 or later
- Recommended libraries:
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`
  - `scipy`

### Setup

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install the necessary libraries:

```powershell
pip install numpy pandas scikit-learn matplotlib seaborn scipy
```

3. Place the dataset in the `data/` folder.

---

## Recommended Workflow

1. **Exploratory Data Analysis**
   - Inspect distributions of transaction features.
   - Visualize balances, purchase frequency, and usage statistics.
   - Identify missing values, correlations, and feature scales.

2. **Preprocessing**
   - Handle missing values using imputation or row removal.
   - Normalize or scale numeric features so clustering works effectively.
   - Select features relevant for anomaly detection.

3. **DBSCAN Clustering**
   - Generate a k-distance plot to choose an appropriate `epsilon`.
   - Experiment with different `MinPts` values.
   - Fit DBSCAN and examine cluster labels.

4. **Outlier Profiling**
   - Identify points labeled as `-1` (noise).
   - Compare noise points to clustered points across key features.
   - Summarize what makes those points anomalous.

---

## Notes

- `DBSCAN` is especially useful when clusters have arbitrary shapes and when the dataset contains noise.
- The `epsilon` parameter controls neighborhood distance; choose it from the k-distance curve.
- `MinPts` should typically be set based on the dimensionality of the data plus one.

---

## Final Deliverables

Recommended final artifacts for this project:
- A cleaned Python script or notebook implementing the full workflow.
- A k-distance plot with the selected `epsilon`.
- A table or chart summarizing cluster sizes and noise count.
- Analysis of anomalous credit card usage behaviors.

---

## Contact

Author : Ankit Kumar <br>
Email : [ankit07chy@gmail.com](mailto:ankit07chy@gmail.com)