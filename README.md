# airbnb-price-predictor
Predictive pricing analysis for New York City Airbnb listings using feature engineering, Lasso regression, and Python.
Predictive pricing analysis developed using New York City Airbnb listing data.

The goal of the project was to identify the factors that influence Airbnb nightly prices and build an interpretable model that could help hosts make more data-informed pricing decisions.

## Project Objective

The analysis explores how property characteristics, location, review activity, and host behaviour influence Airbnb listing prices across New York City.

A predictive pricing model was developed using publicly available NYC Airbnb data.

## What I Did

- Cleaned and preprocessed Airbnb listing data
- Removed invalid listings and handled missing values
- Engineered features including:
  - Days since last review
  - Host portfolio size
  - Neighbourhood and room-type interactions
  - Minimum-night categories
  - Review-volume categories
- One-hot encoded categorical variables
- Log-transformed listing prices to reduce skew
- Standardised numerical features
- Built a Lasso regression model using 5-fold cross-validation
- Analysed model coefficients to identify the strongest drivers of Airbnb pricing
- Built a prediction function for estimating nightly prices from listing characteristics

## Model Performance

The final LassoCV model achieved:

- Test R²: 0.543
- RMSE: approximately $185.96
- Optimal alpha: 0.00023

The model explained approximately 54% of the variation in Airbnb nightly prices using observable listing-level characteristics.

## Key Findings

- Room type was one of the strongest predictors of price
- Manhattan listings generally commanded higher prices
- Individual neighbourhoods were often more informative than borough alone
- Recent review activity was associated with higher prices
- Host behaviour and portfolio size also contributed to pricing differences

## Technologies

Python, Pandas, NumPy, scikit-learn, Lasso Regression, Feature Engineering, Data Visualisation

## Files

- `airbnb_pricing_analysis.ipynb` – data cleaning, feature engineering, modelling, evaluation, and prediction
- `AB_NYC_2019.csv` – source NYC Airbnb dataset
- `airbnb_pricing_analysis_report.pdf` – project report, results, visualisations, and recommendations

## Data

The project uses the publicly available `AB_NYC_2019.csv` dataset containing Airbnb listings across New York City.

The dataset includes listing location, room type, price, minimum stay, review activity, host listing counts, availability, and other listing-level characteristics.
