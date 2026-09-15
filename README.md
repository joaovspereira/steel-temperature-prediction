# Steel Temperature Prediction

End-to-end regression project for a metallurgical process.

## Business problem
Steelproof wants to improve temperature control during secondary steel treatment. A reliable prediction of final steel temperature can support faster and more energy-efficient operational decisions.

## Objective
Predict the final steel temperature from process data with event-time filtering and translating prediction error into operational meaning.

## Saved evaluation results
- **Selected model:** LightGBM
- **MAE:** 5.533 °C
- **RMSE:** 7.481 °C
- **R²:** 0.773
- **MAE reduction vs. mean baseline:** 45.3%

## What the project demonstrates
Data integration, domain-informed cleaning, feature engineering, leakage prevention, regression, hyperparameter tuning, cross-validation, residual analysis and model interpretation.

## Technologies
Python · pandas · NumPy · scikit-learn · LightGBM · Matplotlib · Seaborn · Jupyter

## Repository structure
- [notebooks/steel_temperature_prediction.ipynb](notebooks/steel_temperature_prediction.ipynb) — full analysis
- [data/README.md](data/README.md) — expected data files
- [requirements.txt](requirements.txt) — Python dependencies


## Limitations and next steps
The model is predictive rather than causal. A production version should use only features available at the intended prediction moment, add uncertainty estimates and monitor data/model drift.

## Run locally

Clone the repository, enter its directory and create an environment:

```bash
git clone https://github.com/joaovspereira/steel-temperature-prediction.git
cd steel-temperature-prediction
python -m venv .venv
```

Activate it with `source .venv/bin/activate` on macOS/Linux or `.\.venv\Scripts\Activate.ps1` in Windows PowerShell. Then run:

```bash
python -m pip install -r requirements.txt
python -m notebook notebooks/steel_temperature_prediction.ipynb
```

Place the original datasets listed in [data/README.md](data/README.md) inside `data/` before executing cells. Dataset files are excluded from version control.

## Evaluation scope

The implementation integrates five input tables. Results come from the original saved run on a random 75/25 split, with 1,842 training and 614 test batches. This is retrospective batch prediction: duration, measurement counts and process totals require a feature-availability review before earlier prediction. Material-frequency selection occurred before the split; a future pipeline should fit it inside training only. The metrics do not measure energy savings or prove readiness for operational control.

The publication review checked notebook structure and code syntax, but did not rerun the full training process or establish exact environment reproducibility.

## Learning

This project was developed during the TripleTen Data Science bootcamp. It demonstrates a documented analytical workflow, explicit evaluation criteria and interpretation of model limitations.
