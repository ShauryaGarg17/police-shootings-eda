# Exploratory Data Analysis of Police Shootings (Python)

A course project demonstrating an end-to-end exploratory data analysis workflow in **Python / Google Colab** using a police shootings dataset. The notebook adapts the course's R-based EDA exercises into Python, covering data quality, descriptive statistics, visualisation, time-series exploration, and introductory unsupervised clustering.

> **Scope:** Descriptive, educational analysis of recorded cases. Counts are not population-adjusted rates; correlations and clusters are not causal findings.

## Project contents

```text
police-shootings-eda/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── police_shootings_eda.ipynb
├── data/
│   └── README.md                # dataset acquisition and upload notes
├── reports/
│   └── eda_analysis_outputs.pdf # exported notebook and actual output screenshots
└── docs/
    ├── speaker_notes_with_results.docx
    └── cell_speaker_notes.md
```

## How to run

### Google Colab (recommended)

1. Open `notebooks/police_shootings_eda.ipynb` in Google Colab (upload the notebook or open it from GitHub).
2. Run the cells from top to bottom.
3. When the upload prompt appears, choose the original **`shootings.csv`** file.
4. Review the generated tables and charts.
5. The final export cell can download a `shootings_cleaned.csv` file.

The notebook uses Colab's `google.colab.files` upload/download features, so running it in a local Jupyter environment would require adapting those cells.

### Dependencies

Python 3.10+ recommended. In an environment with Python installed:

```bash
pip install -r requirements.txt
```

Google Colab generally includes the common scientific Python packages, although versions may differ.

## Analysis workflow

| Section | What it covers |
|---|---|
| 1–3 | Imports, dataset loading, initial inspection |
| 4–5 | Missing-value checks, visualisation, and example handling methods |
| 6–9 | Duplicates, text cleaning, data types, derived columns |
| 10–12 | Descriptive statistics, distributions, boxplots, IQR outliers |
| 13–14 | Group comparisons, contingency tables, scatter plots, correlations |
| 15 | Monthly and yearly incident counts |
| 16–18 | K-means, age-only alternative, hierarchical and agglomerative clustering |
| 19–20 | Final data checks and CSV export |

## Selected observations from the submitted output

The PDF in `reports/` is the authoritative snapshot of the executed notebook results. Highlights visible there include:

- The original dataset contains approximately **4,898 rows** and **15 columns**.
- Very low missingness is observed in a few categorical columns, and **no exact duplicate rows** are reported.
- The age summary reports a **median of 35** and an **interquartile range of 18**.
- The `manner_of_death` counts are heavily concentrated in the **`shot`** category.
- The annual chart covers **2015 through part of 2020**; the 2020 total is not directly comparable with complete years.
- `Age_in_5_Years` is mathematically derived from age, so its very high correlation with age is expected.
- The initial K-means example includes **record ID** as a feature, which makes the resulting clusters difficult to interpret substantively. An age-only alternative is included for comparison.

For fuller chart-by-chart interpretation, see `docs/speaker_notes_with_results.docx`.

## Interpretation and limitations

- These records are **not** a random sample of the entire population. Group counts do not establish group-level risk.
- Data completeness, reporting practices, and date coverage may affect apparent trends.
- Missing-value strategies are **demonstrated on separate copies**; they are not all applied sequentially to the final dataset.
- `id` is an identifier, not a meaningful explanatory variable. Its inclusion in correlations or clustering is instructional only.
- Statistical outliers should be investigated rather than assumed to be incorrect.
- The source CSV is not included; reproducibility depends on access to the same input dataset.

## Documentation

- **Executed results:** [`reports/eda_analysis_outputs.pdf`](reports/eda_analysis_outputs.pdf)
- **Presentation notes with output interpretation:** [`docs/speaker_notes_with_results.docx`](docs/speaker_notes_with_results.docx)
- **Additional cell notes:** [`docs/cell_speaker_notes.md`](docs/cell_speaker_notes.md)

## Author

Shaurya Garg — EDA course project.

## Dataset and usage rights

The dataset source and its redistribution license were not provided with the available project files. Check the original source's terms before sharing the CSV publicly. No software license has been assigned to this repository package; add one only after choosing the terms you want.
