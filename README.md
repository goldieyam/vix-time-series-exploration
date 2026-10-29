# VIX Trend Analysis with Python

A coursework exercise exploring historical Volatility Index (VIX) data through visualisation, rolling averages and simple linear regression.

> **Educational demonstration only:** This project is not a validated forecasting tool or investment advice.

## Purpose

Practise preparing time-series data, visualising trends and generating a basic regression estimate.

## Dataset

The script downloads publicly available historical VIX data from the `datasets/finance-vix` GitHub repository, using the `DATE` and `CLOSE` columns.

This is real historical data, not synthetic data. Results may change as the source dataset is updated.

## Data Source

This project retrieves historical VIX data from the `datasets/finance-vix` GitHub repository at runtime; no CSV dataset is included here. The repository identifies CBOE as the original source and declares PDDL for its data package, while noting uncertainty about the original data’s licensing terms.

## Tools

- Python
- pandas
- matplotlib
- scikit-learn
- Google Colab or a compatible Python environment

## Workflow

1. Load the CSV dataset.
2. Convert dates, select relevant columns and rename them.
3. Calculate a seven-observation rolling average.
4. Plot historical values alongside the rolling average.
5. Remove rows containing missing values.
6. Convert dates to numerical values.
7. Fit a linear regression using date as the input and VIX closing value as the target.
8. Generate an estimate for the calendar day after the latest date in the dataset.

## Outputs

- A chart showing VIX closing values and their rolling average.
- A printed regression estimate for the next calendar day after the dataset ends.

## Limitations

| Area | Limitation |
| --- | --- |
| Rolling average | Covers seven observations, not necessarily seven calendar days. |
| Model inputs | Uses date only; the rolling average is not a model input. |
| Evaluation | No separate test set, baseline comparison or accuracy assessment. |
| Model assumptions | A straight-line relationship with date does not capture complex market dynamics. |
| Estimated date | May fall on a weekend or market holiday. |
| Interpretation | The output is a learning demonstration, not evidence of reliable forecasting. |

## Skills Practised

- CSV loading and tabular data manipulation
- Date conversion and missing-value handling
- Rolling calculations and data visualisation
- Introductory regression modelling
- Recognising analytical limitations

## Running the Project

1. Open the script in Google Colab or a compatible Python environment.
2. Ensure `pandas`, `matplotlib` and `scikit-learn` are available.
3. Run the script with internet access to retrieve the dataset.
4. Review the chart and printed estimate alongside the limitations above.
