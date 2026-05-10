# [XAI Project] Prices Prediction
This repository is used for the ML Regression project on Explainable AI in Predictive Modeling course


# ML Regression project

__Data used is from https://www.kaggle.com/datasets/taeefnajib/used-car-price-prediction-dataset__

__Used Car Price Prediction Dataset is a comprehensive collection of automotive information extracted from the popular automotive marketplace website, https://www.cars.com. This dataset comprises 4,009 data points, each representing a unique vehicle listing, and includes nine distinct features providing valuable insights into the world of automobiles.__

### Variables definition:
* Brand & Model: Identify the brand or company name along with the specific model of each vehicle.
* Model Year: Discover the manufacturing year of the vehicles, crucial for assessing depreciation and technology advancements.
* Mileage: Obtain the mileage of each vehicle, a key indicator of wear and tear and potential maintenance requirements.
* Fuel Type: Learn about the type of fuel the vehicles run on, whether it's gasoline, diesel, electric, or hybrid.
* Engine Type: Understand the engine specifications, shedding light on performance and efficiency.
* Transmission: Determine the transmission type, whether automatic, manual, or another variant.
* Exterior & Interior Colors: Explore the aesthetic aspects of the vehicles, including exterior and interior color options.
* Accident History: Discover whether a vehicle has a prior history of accidents or damage, crucial for informed decision-making.
* Clean Title: Evaluate the availability of a clean title, which can impact the vehicle's resale value and legal status.
* Price: Access the listed prices for each vehicle, aiding in price comparison and budgeting.

# Motivation
The used car market is highly dynamic, with prices influenced by a complex interplay of factors such as brand reputation, mileage, model year, fuel type, and overall vehicle condition. However, determining a fair and accurate price is often difficult for both buyers and sellers due to the extreme variability of these features and the presence of high-end luxury outliers.

This project aims to strictly evaluate how different car attributes affect pricing and to build a robust, reproducible machine learning pipeline that can accurately predict the price of a used vehicle, effectively handling the "luxury ceiling" in the market

# Approach
Data Preprocessing & Feature Engineering:

    Dynamic imputation of missing engine_liters, horsepower, and num_gears using grouping hierarchies.

    Target encoding for high-cardinality categorical variables (Brands, Colors, Models) to prevent data leakage between train/test splits.

    Log transformation of the target variable (price) to handle right-skewed price distributions.

Exploratory Data Analysis (EDA): Generating statistical visualizations to identify key drivers of price.

Model Training & Tuning:

    Implementing Linear Regression, Ridge, and Lasso baselines.

    Training advanced non-linear models including Decision Trees and XGBoost.

    Performing hyperparameter tuning via 5-fold Cross-Validation (GridSearchCV).

Evaluation: Assessing model performance using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and Dollar Error Percentages as well as explainable AI practices.

# Findings 

# Repository structure
* Code/
Contains the main Jupyter Notebook used for data preprocessing, feature engineering, model training, evaluation, and explainable AI analysis.
- PricesPrediction.ipynb
Main notebook implementing the used car price prediction workflow, including:
- Data Exploration
- Data cleaning and feature engineering
- Model training
- Performance evaluation
- Explainable AI
* Data/
Stores the dataset used in the project.
- used_cars_.csv
Dataset containing used car listings and features such as brand, model, mileage, fuel type, engine details, and price.
* .gitignore
Specifies files and folders that should be excluded from version control.
* README.md
Provides project overview, setup instructions, repository structure, and usage details.