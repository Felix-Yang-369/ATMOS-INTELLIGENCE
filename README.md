# ATMOS INTELLIGENCE

**English** · [简体中文](./README.zh-CN.md)

![天象智研 ATMOS INTELLIGENCE](./docs/assets/cover.webp)

*Project concept artwork · Created with ImageGen*

**Chinese name: 天象智研.** Recognizing weather conditions from observations and exploring the relationships between data, features, and models.

**Python · Pandas · NumPy · Scikit-learn · Jupyter Notebook**

## Overview

ATMOS INTELLIGENCE is a machine-learning project built around weather data. The public notebook records data cleaning, exploratory analysis, outlier detection, feature-importance analysis, and modeling experiments targeting `condition_text`.

The current primary task is to identify observed weather conditions, such as sunny, cloudy, or rainy, from observation features. Forecasting future weather is a follow-up research direction requiring its own temporal split and validation design.

## Data and Features

The notebook reads `GlobalWeatherRepository.csv`. The original observations include geographic, meteorological, air-quality, and astronomical information. These describe the dataset's fields, not a claim that every field is used by the final model.

| Area | Examples |
| --- | --- |
| Weather observations | Temperature, wind speed, pressure, precipitation, humidity, cloud cover, visibility, and UV index |
| Air quality | Carbon monoxide, ozone, nitrogen dioxide, particulate matter, and air-quality indices |
| Target | `condition_text`, the weather condition associated with an observation |

The random-forest experiment uses numeric weather and air-quality features and encodes the target condition labels. See the notebook for the exact fields and processing steps.

## Experiment Workflow

1. **Clean records:** normalize selected location records and condition labels, then inspect distributions.
2. **Inspect outliers:** apply Isolation Forest to numeric features and construct a filtering mask.
3. **Explore features:** examine visualizations, correlations, and feature importance.
4. **Build models:** the notebook contains several model experiments, including a random-forest classifier with `n_estimators=100` and `random_state=42`.
5. **Analyze outputs:** retain experiment outputs and comparisons as a basis for improving evaluation.

## Evaluation and Next Steps

The existing experiments use a random train/test split. Some evaluation cells still apply regression metrics such as MSE and R² to encoded weather categories. Follow-up work should add classification measures such as accuracy, macro F1, and confusion matrices, and verify feature/label alignment after outlier filtering.

Future-weather forecasting also requires time-based data splits, leakage checks, and comparable baselines. Deep-learning time-series models and a REST API remain planned enhancements.

## Repository Contents

- [`Project_Codes_and_Notes.ipynb`](./Project_Codes_and_Notes.ipynb): experiment code, notes, and existing outputs.
- `README.md`: English documentation.
- [`README.zh-CN.md`](./README.zh-CN.md): Chinese documentation.
- `docs/assets/cover.webp`: project concept poster.

## Viewing and Running

Open the notebook directly on GitHub to inspect its code and existing outputs, or download it for Jupyter Notebook or JupyterLab.

`GlobalWeatherRepository.csv` is not currently included in this repository. Re-execution requires a compatible data file, a checked file path, and dependencies matching the notebook's imports. The environment and execution order have not yet been packaged as a one-command workflow with locked dependencies. Stored outputs do not establish reproducibility in a fresh environment.
