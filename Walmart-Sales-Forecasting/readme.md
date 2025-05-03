# Walmart Sales Time Series Forecasting Using Machine and Deep Learning

Time Series Forecasting of Walmart Sales Data using Deep Learning and Machine Learning.

## Datasets
**Walmart Recruiting - Store Sales Forecasting** dataset downloaded from [Kaggle](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting).

- **train.csv**: Contains 115,064 rows of sales data.
- **stores.csv**: Contains 45 rows of store information.
- **features.csv**: Contains 8,190 rows of additional features.

## Machine Learning Models
- Linear Regression
- Random Forest Regression
- K Neighbors Regression
- XGBoost Regression
- Custom Deep Learning Neural Network

## Data Preprocessing
### Handling Missing Values
- Missing values in CPI, Unemployment, and MarkDown columns were filled using the median.

### Merging Datasets
- Combined `train.csv`, `stores.csv`, and `features.csv` into a single dataset with 421,570 rows and 15 attributes.
- Converted the `Date` column to datetime format and set it as the index.

### Feature Engineering
- Split the `Date` column into Year, Month, and Week.
- Aggregated weekly sales using statistical measures (max, min, mean, median, std).
- Summed markdowns into a single `Total_MarkDown` column.
- Removed outliers using z-score and negative weekly sales, resulting in 374,247 rows and 20 columns.
- Applied one-hot encoding to categorical columns, increasing the total number of columns to 145.
- Normalized numerical columns using MinMaxScaler.

### Recursive Feature Elimination
- Selected 24 important features using Random Forest Regressor.

## Splitting Dataset
- Split the dataset into 80% training and 20% testing.
- Target feature: `Weekly_Sales`.

## Model Performance
### Linear Regression
- Accuracy: 92.28%
- R²: 0.9228
- RMSE: 0.059

### Random Forest Regression
- Accuracy: 97.89%
- R²: 0.9788
- RMSE: 0.03087

### K Neighbors Regression
- Accuracy: 91.97%
- R²: 0.9199
- RMSE: 0.0602

### XGBoost Regression
- Accuracy: 94.21%
- R²: 0.9421
- RMSE: 0.0511

### Custom Deep Learning Neural Network
- Accuracy: 90.50%
- R²: 0.9144
- RMSE: 0.0622

## Model Comparison
| Model                     | Accuracy (%) | R²     | RMSE   |
|---------------------------|--------------|--------|--------|
| Linear Regression         | 92.28        | 0.9228 | 0.059  |
| Random Forest Regression  | 97.89        | 0.9788 | 0.0309 |
| K Neighbors Regression    | 91.97        | 0.9199 | 0.0602 |
| XGBoost Regression        | 94.21        | 0.9421 | 0.0511 |
| Deep Learning Neural Net  | 90.50        | 0.9144 | 0.0622 |

## Citations
- **Walmart Recruiting - Store Sales Forecasting**: [Kaggle Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
