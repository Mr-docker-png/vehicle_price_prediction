🚗 Vehicle Price Prediction

A machine learning regression project that predicts vehicle prices based on vehicle specifications such as make, model, year, engine size, mileage, fuel type, and transmission.

The project focuses on building a complete ML workflow using preprocessing pipelines, Linear Regression, Gradient Boosting, cross-validation, and hyperparameter tuning.

📌 Project Overview

The goal of this project is to predict the price of a vehicle from its available features.

The project compares a simple Linear Regression model with a more advanced Gradient Boosting Regressor and evaluates both using standard regression metrics.

📊 Dataset

The dataset contains 1,000 vehicle records with the following features:

Make
Model
Year
Engine Size
Mileage
Fuel Type
Transmission
Price — target variable
Data Quality
Rows: 1,000
Features: 7 input features
Target: Price
Missing values: None
Duplicate rows: None
🔍 Exploratory Data Analysis

The project includes:

Price distribution analysis
Numerical feature distributions
Mileage vs Price analysis
Engine Size vs Price analysis
Year vs Price analysis
Feature correlation analysis
Average price by:
Make
Model
Fuel Type
Transmission
Important Correlations
Feature	Correlation with Price
Year	0.610
Mileage	-0.557
Engine Size	0.384

This indicates that newer vehicles tend to have higher prices, while higher mileage tends to be associated with lower prices.

⚙️ Preprocessing

A ColumnTransformer was used to handle numerical and categorical features.

Numerical Features
Year
Engine Size
Mileage

These were standardized using:

StandardScaler

Categorical Features
Make
Model
Fuel Type
Transmission

These were converted into numerical representations using:

OneHotEncoder

The preprocessing and model were combined using a Scikit-learn Pipeline.

🤖 Models
1. Linear Regression

Linear Regression was used as the baseline model.

Test Performance:

MAE: 1810.55
RMSE: 2237.29
R²: 0.8171
2. Gradient Boosting Regressor

Gradient Boosting was tested as a more advanced nonlinear model.

Test Performance:

MAE: 1858.07
RMSE: 2299.88
R²: 0.8067
🔧 Hyperparameter Tuning

GridSearchCV with 5-fold cross-validation was used to tune the Gradient Boosting model.

Best parameters:

n_estimators = 100
learning_rate = 0.1
max_depth = 2

Best cross-validation R²:

0.8123

Final tuned Gradient Boosting test performance:

MAE: 1860.92
RMSE: 2311.40
R²: 0.8048
🏆 Model Comparison
Model	MAE ↓	RMSE ↓	R² ↑
Linear Regression	1810.55	2237.29	0.8171
Gradient Boosting	1858.07	2299.88	0.8067
Tuned Gradient Boosting	1860.92	2311.40	0.8048
Final Result

Linear Regression performed best on the test set.

This demonstrates an important machine learning lesson: a more complex model does not necessarily perform better than a simpler model. Model selection should be based on evaluation results.

📈 Actual vs Predicted

The final Linear Regression model was evaluated using an Actual vs Predicted Price visualization.

The predictions generally follow the diagonal reference line, showing a strong relationship between the actual and predicted vehicle prices.

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Scikit-learn
Jupyter Notebook
🧠 ML Concepts Practiced
Exploratory Data Analysis
Feature analysis
Correlation analysis
Train/Test Split
Numerical scaling
One-hot encoding
ColumnTransformer
Pipelines
Linear Regression
Gradient Boosting
Cross-Validation
GridSearchCV
Hyperparameter tuning
Regression evaluation
Model comparison
Prediction visualization

🚀 Future Improvements
Test additional regression algorithms
Perform feature importance analysis
Experiment with different preprocessing strategies
Deploy the model as a web application
Add a vehicle price prediction interface
👨‍💻 Author
Jaskaran Singh

A machine learning project focused on practical understanding of data preprocessing, regression models, pipelines, and model evaluation.
