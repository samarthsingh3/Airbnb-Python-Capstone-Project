# **Airbnb Data Analysis and Prediction**

This repository contains a comprehensive analysis of Airbnb data, including data cleaning, exploratory data analysis, and predictive modeling using various machine learning algorithms. The main goal is to predict Airbnb listing prices based on various features.

## Table of Contents

- [Installation](#installation)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling](#modeling)
  - [Linear Regression](#linear-regression)
  - [Regression Trees](#regression-trees)
  - [Random Forest](#random-forest)
  - [Gradient Boosting](#gradient-boosting)
- [Results](#results)
- [Conclusion](#conclusion)
- [Acknowledgements](#acknowledgements)

## Installation

To run this project, you need to have the following libraries installed:

```python
pandas
numpy
seaborn
matplotlib
scikit-learn
```

You can install these libraries using pip:

```sh
pip install pandas numpy seaborn matplotlib scikit-learn
```

## Dataset

The datasets used in this project are:

- `calendar.csv`
- `hosts.csv`
- `reviews.csv`
- `listings.csv`

These datasets are loaded and preprocessed to remove null values, handle duplicates, and detect outliers.

## Data Preprocessing

1. **Calendar Data**:
   - Removed timestamp from the date column.
   - Filled null values in the price and adjusted price columns with the median.
   - Removed outliers using the Interquartile Range (IQR) method.
   - Checked for duplicates.

2. **Hosts Data**:
   - Removed the `host_about` column.
   - Filled null values in the `host_location` column with the mode.
   - Checked for duplicates.

3. **Listings Data**:
   - Removed unnecessary columns: `description`, `name`, `listing_url`.
   - Filled null values in the `bedrooms` and `beds` columns with the median.
   - Processed the `bathrooms_text` column to extract numerical data.
   - Counted the number of amenities.

4. **Reviews Data**:
   - Removed the `comments` column.
   - Checked for duplicates.

## Exploratory Data Analysis

- Box plots to detect outliers in `price` and `adjusted_price` columns.
- Histograms to visualize the distribution of `Number_of_bathrooms`.
- Bar plots and scatter plots for bivariate analysis of `beds` vs. `price` and `Number_of_bathrooms` vs. `price`.

## Modeling

### Linear Regression

- Applied linear regression to predict `price` based on `bedrooms` and `amenities_element_count`.
- Evaluated model performance using R-squared (R2) and Mean Squared Error (MSE).

### Regression Trees

- Implemented decision tree regressor.
- Evaluated model performance using train/test/validation splits.

### Random Forest

- Applied Random Forest Regressor for prediction.
- Evaluated model performance using train/test/validation splits.

### Gradient Boosting

- Applied Gradient Boosting Regressor for prediction.
- Evaluated model performance using train/test/validation splits.

## Results

- **Linear Regression**: Showed low R2 score indicating poor predictive power.
- **Regression Trees**: Improved performance compared to linear regression.
- **Random Forest**: Provided better R2 scores and lower MSE.
- **Gradient Boosting**: Showed the best performance among the models with highest R2 scores and lowest MSE.

## Conclusion

The analysis showed that the features with the highest predictive power for Airbnb listing prices are `bedroom count`, `accommodation capacity`, `bed count`, `amenities`, and `availability status`. Among the models tested, Gradient Boosting Regressor performed the best.

## Acknowledgements

Special thanks to the Airbnb team for providing the datasets used in this analysis.

---

Feel free to modify and enhance this README according to your specific needs and additional findings.
