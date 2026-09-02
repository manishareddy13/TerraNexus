# TerraNexus

TerraNexus is an Agricultural Intelligence and Market Analytics Platform developed to analyze agricultural production and market data using Python and Machine Learning.

## Week 2 Work

During Week 2, the Telangana agricultural market dataset was cleaned, analyzed, and used for machine learning model development.

After cleaning the market report, the dataset contained:

- 461 valid records
- 64 markets
- 88 commodities
- 10 attributes

The main attributes include Market, Commodity, Arrivals, Variety, Grade, Minimum Price, Maximum Price, Modal Price, and price units.

## Machine Learning Objective

The objective of this analysis is to predict the Modal Price of agricultural commodities using:

- Market
- Commodity
- Variety
- Grade
- Arrivals

The data was divided into:

- Training data: 368 records
- Testing data: 93 records

## Models Used

Three regression models were trained and compared:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

## Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 2687.01 | 8986.40 | -0.171 |
| Decision Tree | 2256.72 | 7955.56 | 0.083 |
| Random Forest | 2041.38 | 7738.77 | 0.132 |

Random Forest performed best among the three models because it gave the lowest MAE and RMSE and the highest R² score.

## Analysis

The modal price distribution was highly right-skewed. Most records were concentrated in the lower price range, while a small number of records had very high modal prices.

Some high-priced commodities had only one observation in the daily market report. Therefore, these values should not be considered as general market trends. More historical market data is required for stronger price prediction and reliable long-term analysis.

## Project Structure

```text
TerraNexus/
├── data/
│   ├── horizontal_year_vertical_crop_report.xls
│   └── Telangana_Market_Report.csv
├── notebooks/
│   └── Week2_ML_Analysis.ipynb
├── results/
│   ├── actual_vs_predicted_random_forest.png
│   ├── modal_price_distribution.png
│   ├── model_performance_comparison.png
│   └── model_results.csv
├── README.md
└── requirements.txt