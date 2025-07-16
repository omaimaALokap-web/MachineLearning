# Graduation-Project-1
## Project Overview
This project aims to predict whether a Near-Earth Object (NEO) is hazardous based on various astronomical features. Accurate prediction of hazardous NEOs is crucial for planetary defense and mitigating potential impacts on Earth.

#### Dataset Description
The dataset comprises information on NEOs, including:

#### Features:
* neo_id: Unique identifier for each NEO.
* name: Name of the NEO.
* absolute_magnitude: Intrinsic brightness of the NEO.
* estimated_diameter_min and estimated_diameter_max: Estimated size range of the NEO.
* orbiting_body: Celestial body around which the NEO orbits.
* relative_velocity: Speed of the NEO relative to Earth.
* miss_distance: Closest distance between the NEO and Earth.

* Target Variable:
is_hazardous: Boolean indicating if the NEO is potentially hazardous.


## Key Steps and Methodologies
###  1. Data Preprocessing
* Handling Missing Values: Missing values in absolute_magnitude, estimated_diameter_min, and estimated_diameter_max were imputed using the median of the respective columns.


* Scaling Numerical Features: Numerical features were scaled using StandardScaler to ensure all features are on the same scale.

* Handling Imbalanced Classes: The target variable is_hazardous was imbalanced. Techniques such as Random Oversampling and SMOTE were applied to balance the dataset.


#### 2. Exploratory Data Analysis (EDA)
* Class Distribution: The target variable is_hazardous was highly imbalanced, with only a small percentage of NEOs classified as hazardous.

* Feature Distributions: Visualizations such as histograms, boxplots, and scatter plots were used to understand the distributions of features like absolute_magnitude, relative_velocity, and miss_distance.

* Correlation Analysis: A correlation heatmap was created to identify relationships between features.

#### 3. Model Selection and Training
* The dataset trained on Logistic Regression, Random Forest, XGBoost, and LightGBM.


#### 4. Model Evaluation
* Metrics: The models were evaluated using precision, recall, F1-score, and AUC-ROC.

* Results: The best-performing model achieved an AUC-ROC score of 0.92 and an F1-score of 0.85 on the test set.

## Key Findings
* Imbalanced Dataset: The dataset was highly imbalanced, with only ~10% of NEOs classified as hazardous. Techniques  Random Oversampling was effective in balancing the dataset.

* Feature Importance: Features like absolute_magnitude and relative_velocity were found to be highly predictive of whether an NEO is hazardous.

* Best Model: The Random Forest model performed the best, achieving high precision and recall for the minority class (hazardous NEOs).
