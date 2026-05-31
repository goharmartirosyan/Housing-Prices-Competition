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

The one-hot encoded model improved the validation MAE by about `$160` compared with my numeric-only Random Forest.

## How to Run

Install the dependencies:

```bash
pip install -r requirements.txt
```

Then open and run:

```text
my_housing_price_model.ipynb
```

## Source

The dataset comes from Kaggle's Housing Prices learning competition.
