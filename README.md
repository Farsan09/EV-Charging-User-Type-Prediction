# EV-Charging-User-Type-Prediction
This project aims to predict user types (e.g., Commuter, Casual Driver, Long-Distance Traveler) based on electric vehicle (EV) charging session data. By leveraging machine learning algorithms, the model helps identify user behavior patterns, which can assist in charging infrastructure optimization, and personalized energy recommendations.
🧩 Objectives

Clean and preprocess EV charging data for modeling.

Handle missing values, categorical variables, and class imbalance.

Compare the performance of multiple ML algorithms.

Select and evaluate the best-performing model.

Generate explainable metrics and visualizations.

📂 Dataset

Source: Internal or open EV charging dataset (e.g., simulated or collected).
Size: ~1,320 records
Features: 480+ after preprocessing

Key Columns
Feature	Description
Charging Duration (hours)	Duration of each charging session
Energy Consumed (kWh)	Total energy used during charging
Charging Rate (kW)	Power level of charging
Charger Type	Type of charger (Level 1 / Level 2 / DC Fast)
Vehicle Model	Type of EV model used
Charging Station Location	Location ID of station
User Type (Target)	Label indicating type of user behavior
⚙️ Data Preprocessing

Missing Values:

Imputed using column mean or most frequent value.

Categorical Encoding:

Converted categorical features into dummy variables using pd.get_dummies().

Feature Scaling (optional):

Applied standard scaling where needed.

Class Imbalance Handling:

Used SMOTE (Synthetic Minority Oversampling Technique) to balance user type classes.

Train-Test Split:

Data split into 80% training and 20% testing.

🧠 Machine Learning Models

The following models were trained and compared:

Model	Description	Library
Logistic Regression	Multinomial classification using softmax	scikit-learn
Random Forest	Ensemble-based decision tree model	scikit-learn
K-Nearest Neighbors (KNN)	Instance-based classifier	scikit-learn
XGBoost Classifier	Gradient-boosted decision trees	XGBoost

📈 Visualizations

Error Rate vs. K Value (KNN tuning)

Confusion Matrix for each model

Feature Importance (for tree-based models)

Class Distribution Before & After SMOTE

Insights

XGBoost provided the most balanced performance across all metrics.

Battery Capacity and energy consumed were the most influential features.

SMOTE effectively mitigated class imbalance issues, improving minority user class recall.


Models were evaluated on accuracy, precision, recall, and F1-score using the test set.

Example code used for evaluation:
