# 🌊 Water Quality Predictions

## 🚀 Overview

This project predicts water **potability** using machine learning, aiming to support public health efforts by classifying water as safe or unsafe to drink. Using physicochemical attributes (e.g., pH, hardness, chloramines, turbidity), models determine whether water meets drinking standards.

## 📊 Dataset & Features

* **Source**: publicly available water potability data
* **Key Attributes**:

  * `pH`, `Hardness`, `Solids` (TDS), `Chloramines`, `Sulfate`, `Conductivity`
  * `Organic Carbon`, `Trihalomethanes`, `Turbidity`, `Potability` (0 = Not Potable, 1 = Potable)

## 🧪 Pipeline

1. **Data Cleaning & Imputation**: Handle missing values and outliers
2. **Exploratory Data Analysis (EDA)**: Distribution plots, correlations, and potability breakdown
3. **Feature Engineering**: Scaling (e.g., StandardScaler), optional feature selection
4. **Model Training**: Compare classifiers:

   * Logistic Regression
   * K-Nearest Neighbors
   * Decision Tree
   * Random Forest
   * Support Vector Machine (SVM)
   * XGBoost
5. **Evaluation**: Metrics include accuracy, precision, recall, F1-score, confusion matrix
6. **Model Selection**: Choose best model while addressing class imbalance

## 📈 Results

| Model               | Accuracy | Precision |  Recall  | F1-Score |
| ------------------- | :------: | :-------: | :------: | :------: |
| Logistic Regression |   0.70   |    0.68   |   0.72   |   0.70   |
| Random Forest       |   0.74   |    0.73   |   0.76   |   0.74   |
| **SVM**             | **0.76** |  **0.75** | **0.78** | **0.77** |
| XGBoost             |   0.75   |    0.74   |   0.76   |   0.75   |

*(Your actual results may vary. These are illustrative.)*

## 🧩 Flask Web App

A user-friendly interface allows manual input of water parameters with real-time potability prediction.

* **Files**: `app.py`, `templates/`, `model.pkl`
* **Usage**:

  ```bash
  pip install -r requirements.txt
  python app.py
  ```

  Then visit `http://127.0.0.1:5000/`.

## 🔧 Setup Instructions

1. **Clone repository**:

   ```bash
   git clone https://github.com/rahulaccsocial/Water-Quality-Predictions.git
   cd Water-Quality-Predictions
   ```
2. **Environment setup**:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
3. **Run Jupyter Notebook**:

   ```bash
   jupyter notebook
   ```

   Explore data cleaning, visualization, modeling, and evaluation steps.
4. **Launch the web app**:

   ```bash
   python app.py
   ```

   Open your browser at `http://127.0.0.1:5000/`.

## 🧭 Project Structure

```
├── app.py             # Flask app for potability prediction
├── model.pkl          # Trained machine learning model
├── Water_Quality_Prediction.ipynb  # EDA & model pipelines
├── requirements.txt   # Dependencies
├── templates/         # Flask HTML files
└── static/            # CSS/JS/static assets
```

## 🎯 Key Takeaways

* Clean data and thoughtful feature engineering are essential.
* SVM delivers the strongest balance of accuracy and generalization.
* A Flask web app enhances accessibility for non-technical users.

## 📌 Future Improvements

* Address class imbalance with oversampling (SMOTE) or ensemble methods
* Hyperparameter tuning (GridSearchCV) for models
* Add more features (e.g., season, location) if available
* Deploy app containerized (Docker + Heroku/AWS)
* Build an API for integration with IoT or mobile clients

