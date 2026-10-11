# Data Analysis & Machine Learning — Synthetic Health Dataset

A Python data-analysis and binary-classification project exploring a synthetically generated dataset of health-related and behavioral attributes. It covers dataset creation, exploratory data analysis, missing-value handling, visualizations, and evaluation of a logistic regression baseline.

**Important:** This is an educational demonstration using synthetic data, not a validated medical prediction system. The `disease` labels are randomly generated, so the model's output should not be interpreted as medically meaningful.

**Tech stack:** Python, pandas, NumPy, seaborn, Matplotlib, scikit-learn.

## Dataset

The data generator creates **700 synthetic rows**, split into **500 training** and **200 testing** samples. Fields include age, sex, smoking, alcohol consumption, exercise frequency, systolic blood pressure, cholesterol, blood sugar, and a binary `disease` label. Missing values are introduced into the feature columns.

## Project files

- `Partea1/Surse/generate_data.py` — generates synthetic data and saves the train/test CSV files.
- `Partea1/Surse/full_program.py` — performs exploratory analysis, handles missing values, makes plots, and evaluates the baseline classifier.
- `Partea1/train_data.csv` and `Partea1/test_data.csv` — data files used by the analysis.
- `Partea1/README.pdf` — original detailed coursework report, including methods, figures, and interpretations (Romanian).

## Setup and execution

Install the dependencies used by the scripts:

```bash
python -m pip install pandas numpy seaborn matplotlib scikit-learn
```

Because the scripts use relative paths for CSV files, run them **from `Partea1`**:

```bash
cd Partea1
python Surse/full_program.py
```

If you want to regenerate the sample data first (this overwrites the CSV files in that directory):

```bash
python Surse/generate_data.py
python Surse/full_program.py
```

The analysis creates graphical outputs in the current working directory.

## Methodology

1. Generate the synthetic features and the randomly assigned binary target.
2. Split the dataset into training and test CSV files.
3. Examine missing values and numerical/categorical distributions.
4. Fill missing numerical features with their means and categorical features with their modes as implemented in the provided script.
5. Produce exploratory plots and descriptive statistics.
6. Train and evaluate a logistic regression classifier using classification metrics and visualizations.

For the original, more detailed analysis and charts, see [`Partea1/README.pdf`](Partea1/README.pdf). This README is an overview; the PDF contains the full report.

## Limitations

- The dataset is synthetic and the label is not derived from the medical attributes.
- Reported classification metrics are therefore not evidence of clinical predictive performance.
- The code and report are preserved as an academic learning project; no production or clinical readiness is claimed.
