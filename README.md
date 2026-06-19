📊 Customer Churn Prediction & Comparative Machine Learning Dashboard

🔗 Live App: khairbakshnoor-pixel-customer-churn-dashboard--app-fhelsw.streamlit.app

https://khairbakshnoor-pixel-customer-churn-dashboard--app-fhelsw.streamlit.app/

An end-to-end Machine Learning web application that predicts whether a telecom customer will Churn or Retain, built with Streamlit. The app trains and compares 6 ML algorithms live, and provides an interactive prediction system for individual customers.


📌 Overview

Customer churn is one of the biggest revenue challenges for subscription-based businesses. Acquiring a new customer costs significantly more than retaining an existing one. This project builds a complete ML pipeline — from raw data to a deployed, interactive dashboard — that helps identify high-risk customers before they leave, enabling proactive retention strategies.


🚀 Features


Home Page — Project overview and navigation guide
Dataset Explorer — Searchable data grid, statistical summary, null counts, and data type inspection
EDA Dashboard — Interactive Plotly visualizations covering churn distribution, contract type, payment method, internet service type, and correlation analysis
Model Training — Train all 6 ML models with a single click and inspect individual model metrics
Model Comparison Dashboard — Live leaderboard ranking all models across 5 key metrics
Prediction System — Enter a single customer's details and get an instant Churn/Retain prediction with a confidence score



📂 Dataset

Telco Customer Churn Dataset (Kaggle)


Shape: 7,043 rows × 20 columns
Includes customer demographics, account information, subscribed services, and billing details



🤖 Machine Learning Models

Six classification algorithms were trained and benchmarked on the same preprocessed dataset:

ModelPurpose / CharacteristicsLogistic RegressionInterpretable linear classification baselineDecision TreeCaptures non-linear relationships via split rulesRandom ForestBagging ensemble that reduces overfittingK-Nearest Neighbors (KNN)Classifies based on distance and local densitySupport Vector Machine (SVM)Maximum-margin decision boundaryGradient BoostingSequential boosting trees for high accuracy


📈 Model Comparison Results

ModelAccuracyPrecisionRecallF1ROC-AUCGradient Boosting0.80620.67350.52410.58950.8432Logistic Regression0.80550.65720.55880.6040.8419Random Forest0.80270.660.52940.58750.84SVM0.79130.64180.4840.55180.7905KNN0.76370.55270.57490.56360.7885Decision Tree0.72890.48960.50530.49740.6573

🏆 Champion Model: Gradient Boosting — highest ROC-AUC (0.8432), indicating the best overall ability to distinguish churned vs. retained customers.


🛠️ Tech Stack


Language: Python
Web Framework: Streamlit
ML Library: Scikit-learn
Data Handling: Pandas, NumPy
Visualization: Plotly
Model Serialization: Joblib / Pickle



📁 Project Structure

project/
│
├── data/                  # Raw dataset (CSV)
├── notebooks/             # EDA, preprocessing, and modeling notebooks
├── models/                # Saved trained model files (.pkl)
├── visuals/                # Dashboard screenshots
│
├── app.py                 # Main Streamlit application
├── utils.py                # Helper functions (data loading, preprocessing)
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation


⚙️ Installation & Local Setup

Clone the repository and run the app locally:

bashgit clone https://github.com/khairbakshnoor-pixel/customer-churn-dashboard.git
cd customer-churn-dashboard
pip install -r requirements.txt
streamlit run app.py

The app will open automatically in your browser at http://localhost:8501


📊 Key EDA Insights


Overall churn rate: 26.5% of customers churned vs. 73.5% retained
Month-to-month contracts show significantly higher churn than one-year or two-year contracts
Customers using electronic check payment methods show higher churn tendency
Fiber optic internet customers churn at a higher rate compared to DSL users



🔮 Future Improvements


Add hyperparameter tuning via GridSearchCV for all models
Integrate SHAP values for explainable predictions
Add SMOTE-based class balancing experiments
Extend with AdaBoost / CatBoost / LightGBM comparisons



👤 Author

Khair Baksh Noor
🔗 LinkedIn | 🔗 GitHub
