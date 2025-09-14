# EPS Beat/Meet/Miss Prediction

## Project Overview
Public companies report their earnings every quarter. Investors and analysts are interested in predicting whether a company will **beat, meet, or miss analysts’ EPS estimates** before the announcement. This project aims to build a machine learning model to classify earnings outcomes based on historical EPS data, analyst estimates, and related financial indicators.

## Team Members
| Name                | Roll Number |
|---------------------|-------------|
| Aadvik Mehrotra     | 2311101     |
| Garvit Saraf        | 2311136     |
| Gourav Pandey       | 2311139     |
| Nitai Satapathy     | 2311163     |
| Rakshith Kumar V    | 2311175     |
| Saksham Gupta       | 2311183     |
| Sanchet Gutgutia    | 2311184     |
| Suryansh Sharma     | 2311191     |
| Tanish Atreya       | 2311193     |


## Problem Statement
- **Objective:** Predict whether a company will **Beat, Meet, or Miss** EPS expectations.
- **Input Features:** 
  - EPS Estimate
  - Previous Reported EPS
  - Surprise (%)  
- **Target:** EPS Outcome (Beat / Meet / Miss)
---

## Dataset
- Collected historical earnings data for S&P 500 companies using **Yahoo Finance API**.
- Dataset Shape: `(5697, 6)`  
- Features include: `Ticker`, `Earnings Date`, `EPS Estimate`, `Reported EPS`, `Surprise (%)`, `Event Type`
- Target variable: `Result` (Beat, Meet, Miss)

---

## Methodology
1. **Data Collection**: Pull EPS history for S&P 500 companies.
2. **Data Preprocessing**: Clean data, create target labels (Beat/Meet/Miss), handle missing values.
3. **Model Building**: Train classifiers including:
   - Decision Tree
   - Random Forest
   - K-Nearest Neighbors (KNN)
   - Support Vector Machine (SVM)
   - Gradient Boosting Classifier
4. **Hyperparameter Tuning**: Optimize model parameters using GridSearchCV.
5. **Evaluation**:
   - Train/Test Split
   - Cross-validation
   - Metrics: Accuracy, F1-score (weighted), Confusion Matrix
6. **Feature Importance**: Identify which features contribute most to the predictions.
7. **Visualization & Results**: Plot feature importance, confusion matrix, and model comparisons.

---

## Workflow
```mermaid
flowchart TD
    A[Start] --> B[Collect Earnings Data from Yahoo Finance]
    B --> C[Preprocess Data]
    C --> D[Create Target Labels: Beat, Meet, or Miss]
    D --> E[Split Data: Train/Test + Cross-Validation]
    E --> F[Train Models: Decision Tree, Random Forest, KNN, SVM, Gradient Boosting]
    F --> G[Hyperparameter Tuning with GridSearchCV]
    G --> H[Evaluate Models: Accuracy & F1 Score]
    H --> I[Feature Importance & Confusion Matrix]
    I --> J[Compare Models & Select Best Model]
    J --> K[Business Implications & Insights]
    K --> L[End]

## Model Performance

- **Weighted F1-score Requirement:** ≥ 0.86
- **Models Evaluated:** Decision Tree, Random Forest, KNN, SVM, Gradient Boosting
- Cross-Validation & Test Results included in the notebook.

## Tools & Libraries

- **Python (Jupyter Notebook)**
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn, yfinance

## Business Implication

- Helps investors make informed decisions before earnings announcements.
- Can be integrated into investment platforms for pre-earnings alerts.
- Shows which features (e.g., Surprise %) drive earnings prediction the most.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.