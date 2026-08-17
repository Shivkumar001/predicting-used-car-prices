# 🚗 Used Car Price Prediction

An end-to-end machine learning project that predicts used car prices using exploratory data analysis, feature engineering, multiple regression algorithms, cross-validation, hyperparameter tuning, and SHAP-based model explainability.

---

## 📌 Project Overview

The used-car market contains many factors that influence vehicle pricing, including vehicle age, kilometers driven, brand, fuel type, transmission, and body style.

The objective of this project is to build and evaluate machine learning models that can estimate used-car prices from available vehicle characteristics and identify the factors that have the greatest influence on resale value.

---

## 🎯 Objectives

* Understand the factors influencing used-car prices.
* Perform comprehensive exploratory data analysis.
* Clean and preprocess the dataset.
* Engineer meaningful features for prediction.
* Compare multiple regression algorithms.
* Use 5-fold cross-validation for more reliable evaluation.
* Perform hyperparameter tuning using `RandomizedSearchCV`.
* Explain model predictions using SHAP.
* Analyze model errors and residuals.
* Translate model findings into practical pricing recommendations.

---

## 📊 Dataset

The project uses a used-car dataset containing vehicle attributes and their corresponding prices.

Key features include:

* Car age
* Kilometers driven
* Brand
* Fuel type
* Transmission
* Body style
* Other vehicle characteristics

The dataset and data dictionary are included in this repository.

---

## 🔎 Exploratory Data Analysis

The analysis investigates:

* Distribution of used-car prices
* Relationship between vehicle age and price
* Relationship between kilometers driven and price
* Price differences across transmission types
* Price differences across fuel types
* Price patterns across body styles
* Brand-level pricing patterns
* Feature correlations
* Potential outliers and skewed variables

The notebook contains the complete visual analysis and supporting interpretations.

---

## ⚙️ Feature Engineering & Preprocessing

The preprocessing pipeline includes:

* Data cleaning
* Missing-value handling
* Feature transformation
* Numerical feature preprocessing
* Categorical feature encoding
* Vehicle age calculation/usage
* Preparation of features for machine learning models

A consistent preprocessing pipeline was used during model development to reduce the risk of data leakage.

---

## 🤖 Models Evaluated

The following regression models were compared:

1. Ridge Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. XGBoost Regressor
5. LightGBM Regressor
6. Tuned LightGBM Regressor

Model performance was evaluated using:

* R²
* MAE
* RMSE
* MAPE

5-fold cross-validation was also used to assess model stability.

---

## 📈 Model Performance

The final hold-out test-set comparison produced the following results:

| Model                   |   Test R² |        Test MAE |
| ----------------------- | --------: | --------------: |
| 🏆 **Ridge Regression** | **0.819** | **₹1.22 Lakhs** |
| XGBoost                 |     0.772 |     ₹1.36 Lakhs |
| Random Forest           |     0.668 |     ₹1.59 Lakhs |
| LightGBM                |     0.649 |     ₹1.80 Lakhs |
| LightGBM (Tuned)        |     0.623 |     ₹1.82 Lakhs |
| Decision Tree           |     0.454 |     ₹2.09 Lakhs |

### 🏆 Best Performing Model

**Ridge Regression** achieved the highest test-set R² of **0.819** and the lowest test MAE of approximately **₹1.22 Lakhs** among the evaluated models.

An important finding from the comparison is that the more complex boosting models did not outperform the regularized linear baseline on this dataset.

---

## 🧠 Model Explainability

SHAP was used to improve model interpretability and understand how important features contribute to predictions.

The analysis helps identify the vehicle characteristics that have the strongest influence on predicted prices.

The repository includes the generated SHAP summary visualization:

**[`shap_summary.png`](shap_summary.png)**

---

## 🔑 Key Business Insights

### 1. Vehicle Age

Vehicle age is one of the strongest factors affecting resale price. Older vehicles generally experience substantial depreciation.

### 2. Kilometers Driven

Higher mileage is generally associated with lower resale prices because greater usage can reduce perceived vehicle value.

### 3. Transmission

Transmission type contributes to differences in vehicle pricing and should be considered when estimating resale value.

### 4. Body Style

Vehicle body style influences pricing, with certain high-demand segments commanding higher prices.

### 5. Fuel Type

Fuel type contributes to differences in resale value across vehicle segments.

### 6. Brand

Brand reputation and resale demand can have a meaningful impact on used-car prices.

---

## 💼 Business Recommendations

* Use vehicle age and kilometers driven as important inputs when setting initial prices.
* Segment vehicles by brand, transmission, fuel type, and body style when analyzing inventory.
* Use machine learning predictions as a supporting tool for pricing decisions.
* Identify vehicles that are significantly over- or under-priced relative to model predictions.
* Retrain and evaluate the model periodically as market conditions and customer preferences change.

---

## 📁 Project Structure

```text
predicting-used-car-prices/
│
├── used_car_price_prediction.ipynb
├── used_cars.csv
├── data_dictionary.docx
├── shap_summary.png
├── project_presentation.pptx
├── README.md
├── .gitignore
└── .gitattributes
```

---

## 🛠️ Technologies Used

**Programming & Data Analysis**

* Python
* Pandas
* NumPy

**Machine Learning**

* Scikit-learn
* XGBoost
* LightGBM

**Visualization**

* Matplotlib
* Seaborn

**Model Explainability**

* SHAP

**Development Environment**

* Jupyter Notebook

**Version Control**

* Git
* GitHub

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Shivkumar001/predicting-used-car-prices.git
cd predicting-used-car-prices
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm shap jupyter
```

### 3. Launch Jupyter

```bash
jupyter notebook
```

### 4. Open

```text
used_car_price_prediction.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model evaluation.

---

## 📄 Additional Project Materials

* 📓 **[Complete Jupyter Notebook](used_car_price_prediction.ipynb)**
* 📊 **[Project Presentation](project_presentation.pptx)**
* 📖 **[Data Dictionary](data_dictionary.docx)**
* 🧠 **[SHAP Summary](shap_summary.png)**
* 📁 **[Dataset](used_cars.csv)**

---

## 📌 Final Takeaway

This project demonstrates a complete machine learning workflow for used-car price prediction, from exploratory analysis and preprocessing through feature engineering, model comparison, cross-validation, hyperparameter tuning, explainability, and business interpretation.

The final evaluation shows that **Ridge Regression achieved the strongest test-set performance with an R² of 0.819**, demonstrating that a well-regularized linear model can outperform more complex ensemble methods on this particular dataset.

---

##  Author

**Shiv Kumar**

Data Analyst 

**Skills:** Python • SQL • Power BI • Excel • Machine Learning • Pandas • NumPy • Tableau 

---

⭐ If you find this project useful, feel free to explore the notebook and project materials.
