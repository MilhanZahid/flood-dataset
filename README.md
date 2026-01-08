This project uses historical flood data (1970–2012) to predict the number of medical camps required in affected regions based on socio-demographic and damage-related features. The model helps decision-makers allocate resources effectively during disaster relief operations.

**Objective:**
Collect and clean historical flood data.
Build a predictive model to forecast the number of medical camps needed during floods.
Evaluate model performance to ensure reliable predictions for disaster planning.

**Data Sources**
Primary source: Pakistan Disaster Management Authority (PDMA)
Supplementary sources: Local regional flood records (district-level data)
Target variable: medical_camps

**Stack:**
Libraries Used:

pandas, numpy → data manipulation
matplotlib, seaborn → visualization
scipy.stats → statistical analysis
scikit-learn → preprocessing, Random Forest, cross-validation, hyperparameter tuning
joblib → model saving/loading

**Methodology:**
Data Preprocessing: Handle missing values, zeros, and outliers. Apply log transformation and clipping on the target variable.
Exploratory Data Analysis: Visualize feature distributions and correlations to understand data patterns.
Model Training: Train a baseline Random Forest, then perform hyperparameter tuning using RandomizedSearchCV.
Model Evaluation: Evaluate train and test sets using MAE, RMSE, and R² metrics. Test metrics are reliable due to internal CV during hyperparameter tuning.
Model Saving: Save the final tuned model using joblib for future predictions.

