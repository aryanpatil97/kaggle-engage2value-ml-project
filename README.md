# Engage2Value: Purchase Value Prediction from Digital Behavior

## Project Overview
This project presents a machine learning pipeline developed as part of the IIT Madras BS Data Science coursework, focusing on predicting customer purchase value based on multi-session digital interaction data. The work was completed for the Kaggle competition **“Engage2Value: From Clicks to Conversions”**, where the objective is to estimate purchase value from anonymized session-level user behavior.

The solution models customer interactions across sessions using behavioral, device, traffic, and geographic attributes to predict transaction value. By combining structured data preprocessing, feature engineering, and modern gradient boosting techniques, the project demonstrates an end-to-end workflow for solving large-scale regression problems in e-commerce analytics.

The notebook is designed to be reproducible and competition-ready, covering data exploration, preprocessing, model experimentation, optimization, validation, and submission generation.

---

## Problem Statement
Digital commerce platforms collect extensive session-level behavioral data, including browsing activity, acquisition channels, device characteristics, and location information. The challenge is to leverage this data to predict how much a user is likely to spend in a session.

Accurate predictions enable businesses to:
- Identify high-value customers,
- Optimize marketing spend,
- Personalize user engagement,
- Improve conversion strategies.

The competition evaluates predictions using the **R² score**, measuring how well predicted values approximate actual purchase values.

---

## Dataset Description
The dataset contains session-level records from an e-commerce environment, including user engagement signals and contextual attributes. Each record represents a session with anonymized information such as:

- Session engagement metrics (page views, hits, visits)
- Device and browser characteristics
- Traffic and marketing acquisition channels
- Geographic attributes
- Multi-session identifiers
- Purchase value target variable

The training dataset includes purchase values, while the test dataset requires predictions for submission.

---

## Methodology
The project follows a structured machine learning workflow:

### Exploratory Data Analysis
Comprehensive EDA was conducted to understand data distributions, conversion rates, missing patterns, and behavioral relationships. Purchase value showed heavy skewness with a high proportion of zero-value sessions, requiring careful preprocessing.

### Feature Engineering
A major component of the project involved generating behavior-driven features capturing engagement intensity, session quality, temporal patterns, and interaction ratios. Additional transformations included logarithmic scaling, ranking, binning strategies, and interaction-based variables. This step significantly expanded predictive information within the dataset.

### Data Preparation
Missing values were handled using business-driven assumptions, categorical values were standardized, and numeric features were scaled using robust scaling techniques. High-cardinality categorical features were simplified to maintain model efficiency.

### Model Development
Multiple regression models were trained and compared, including linear models and gradient boosting approaches. Tree-based boosting models demonstrated superior performance by capturing non-linear patterns within user behavior data.

### Hyperparameter Optimization
Several optimization experiments were conducted on top-performing models to improve predictive performance while maintaining computational efficiency.

### Validation Strategy
Stratified validation splits and cross-validation ensured consistent model evaluation while preserving purchase distribution characteristics across folds.

### Final Model & Submission
The best-performing model was retrained on the full dataset, predictions were generated for test sessions, and outputs were formatted according to Kaggle submission requirements.

---

## Results
The final solution achieved strong predictive performance, with validation and cross-validation results demonstrating stable learning behavior. Feature engineering contributed significantly to performance improvements, and gradient boosting methods consistently outperformed linear baselines.

Prediction outputs showed realistic distributions, successfully capturing both zero-purchase sessions and high-value transactions.

---

## Key Insights
Analysis revealed strong relationships between session engagement depth, repeat visits, browsing intensity, and purchase likelihood. Time-of-day patterns, channel interactions, and device behaviors also contributed to predictive power.

These insights highlight opportunities for marketing optimization, user segmentation, and conversion-focused engagement strategies in real-world commerce applications.

---

## Technologies Used
- Python
- Pandas & NumPy
- Scikit-learn
- XGBoost
- LightGBM
- Matplotlib & Seaborn
- Kaggle Notebook Environment

---

## Learning Outcomes
This project strengthened practical skills in data preprocessing, feature engineering, regression modeling, performance tuning, and validation strategies. It also provided hands-on experience working with large behavioral datasets and designing scalable ML pipelines for real-world prediction problems.

---

## Author
Developed as part of the IIT Madras BS Degree in Data Science program to demonstrate practical machine learning workflow implementation and predictive analytics expertise.
