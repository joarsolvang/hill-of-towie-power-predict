# hill-of-towie-power-predict

This repository contains the workings towards a submission to the [Hill of Towie Wind Turbine Power Prediction](https://www.kaggle.com/competitions/hill-of-towie-wind-turbine-power-prediction) kaggle competition. 

A notebook containing a starting point for a submission can be found in [examples/predict_power.ipynb](examples/predict_power.ipynb). This script uses the [HistGradientBoostingRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.HistGradientBoostingRegressor.html) and some feature engineering.

Work is ongoing to identify weaknesses in the model and introduce additional features. The current aim is to tune a wake model, available through ['floris'](https://github.com/NREL/floris), using the operational data. The intention is to add a theoretical twin to the features to help it identify reduced operating modes and downtime. 

## Data Access

Data is retrieved using [kagglehub](https://github.com/Kaggle/kagglehub). 

### Setup Kaggle API
1. Create a Kaggle account
2. Generate an API token following the [Kaggle API documentation](https://www.kaggle.com/docs/api)
3. Place your `kaggle.json` credentials file in `~/.kaggle/` (Linux/Mac) or `C:\Users\<username>\.kaggle\` (Windows)

## Development
The development environment should be created and managed using [uv](https://docs.astral.sh/uv/). To create the environment:
```commandline
uv sync
```
To run the formatting, linting and testing:
```commandline
uv run poe all
```
Or simply
```commandline
poe all
```
if you have activated the virtual environment (VSCode will do this automatically for you). For example, to activate the environment from a PowerShell prompt:
```powershell
. ".venv\Scripts\activate.ps1"
```

