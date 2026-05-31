# Housing Prices Model

This project is my own extension of Kaggle's Housing Prices machine learning exercise.

I started from the guided exercise, then built a cleaner version that:

- uses a train/validation split to test predictions locally
- checks numeric feature correlations with `SalePrice`
- handles missing numeric values with median imputation
- trains a Random Forest model using more features than the starter notebook
- evaluates the model with Mean Absolute Error
- visualizes the most important model features

## Files

- `housing_price_model.ipynb` - my cleaned notebook and main project work
- `house_data.csv` - housing dataset used by the notebook
- `requirements.txt` - Python packages needed to run the notebook

## Results

| Model | Features Used | Missing Values | Validation MAE |
|---|---:|---|---:|
| Kaggle starter Random Forest | 7 numeric features | not handled separately | `$21,857` |
| My numeric Random Forest | all numeric features | median imputation | `$16,925` |
| My one-hot encoded Random Forest | numeric + categorical features | median/mode imputation | `$16,765` |
| My one-hot encoded XGBoost model | numeric + categorical features | median/mode imputation | `$14,329` |

The XGBoost model improved the validation MAE by about `$2,436` compared with my one-hot encoded Random Forest.

## How to Run

Install the dependencies:

```bash
pip install -r requirements.txt
```

Then open and run:

```text
housing_price_model.ipynb
```

On macOS, XGBoost may also require the OpenMP runtime:

```bash
brew install libomp
```

## Source

The dataset comes from Kaggle's Housing Prices learning competition.

## Note

GitHub may occasionally have trouble rendering Jupyter Notebook previews directly in the browser. If the notebook does not display correctly, please download housing_price_model.ipynb and open it locally using Jupyter Notebook, JupyterLab, VS Code, or upload it to Kaggle to view the full notebook.
