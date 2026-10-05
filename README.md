Power System Load Type Prediction

Overview

This project develops a machine learning classification model to predict the load type of a power system using historical energy consumption and operational data.

The target variable, Load_Type, contains three categories:

* Light_Load
* Medium_Load
* Maximum_Load

Objective

The primary objectives of this project are to:

* Analyze historical power system data.
* Perform data preprocessing and exploratory data analysis.
* Engineer useful time-based features.
* Train multiple machine learning classification models.
* Evaluate model performance using classification metrics.
* Identify the best-performing model for load type prediction.

Dataset

The dataset contains approximately 35,000 observations from 2018.

The major features include:

* Date and time
* Energy consumption (Usage_kWh)
* Lagging reactive power
* Leading reactive power
* CO₂ emissions
* Lagging power factor
* Leading power factor
* Number of seconds from midnight (NSM)
* Load type

Methodology

The project follows these major steps:

1. Data loading
2. Data understanding
3. Data cleaning
4. Exploratory data analysis
5. Feature engineering
6. Time-based train-test splitting
7. Model training
8. Model evaluation
9. Model comparison
10. Feature importance analysis
11. Final prediction

Data Preprocessing

Missing numerical values are handled using median imputation.

The median is calculated using only the training data and then applied to the test data to prevent data leakage.

Time-based features such as month, day, hour, minute, day of week, and weekend indicator are extracted from the date-time column.

Validation Strategy

Because the dataset is time-dependent, a chronological validation strategy is used.

* Training data: January 2018 – November 2018
* Test data: December 2018

The final month is kept completely unseen during model training.

Machine Learning Models

The following classification algorithms are evaluated:

* Logistic Regression
* Random Forest Classifier
* Support Vector Machine
* Gradient Boosting Classifier

Evaluation Metrics

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

Results

The models are compared based on their performance on the unseen December 2018 test data. The model with the highest F1-score is selected as the final model.

Project Structure

power-system-load-type-prediction/
│
├── Power_System_Load_Type_Prediction.ipynb
├── load_data.csv
└── README.md

Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Jupyter Notebook

Conclusion

This project demonstrates how machine learning can be applied to historical power system data to classify different load conditions. A time-based evaluation strategy ensures that the model is tested on recent unseen observations, providing a more realistic assessment of its generalization capability.
