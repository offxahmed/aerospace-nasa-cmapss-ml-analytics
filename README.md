# AI-Based Predictive Maintenance for Aircraft Turbofan Engines

**A Machine Learning Project using NASA Turbofan Engine Degradation Dataset**

---

## 📋 Project Overview

This project develops a **Machine Learning system** to predict the **Remaining Useful Life (RUL)** of aircraft turbofan engines. By analyzing sensor data, the model can predict when an engine is likely to fail, enabling **predictive maintenance** instead of scheduled or reactive maintenance.

This approach is widely used in the aerospace industry by companies like **GE Aviation, Rolls-Royce, Boeing, and Airbus** to reduce downtime, save costs, and improve safety.

**Goal**: Predict the number of cycles left before an engine fails using classical Machine Learning algorithms.

---

## ✨ Key Features

- Data preprocessing and feature engineering for time-series sensor data
- Exploratory Data Analysis (EDA) with visualizations
- Multiple Machine Learning models comparison
- Remaining Useful Life (RUL) prediction
- Model performance evaluation using regression metrics
- Simple web interface for predictions (optional Streamlit app)
- Focus on **explainability** and practical aerospace application

---

## 📊 Dataset

- **Source**: NASA Prognostics Center of Excellence (PCoE)
- **Dataset**: CMAPSS (Commercial Modular Aero-Propulsion System Simulation)
- **Subset Used**: FD001 (One operating condition)
- **Content**:
  - 21 sensor measurements
  - 3 operational settings
  - Engine run-to-failure cycles
- **Total Training Engines**: 100
- **Total Test Engines**: 100

**Link**: [NASA Turbofan Dataset](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/#turbofan)

---

## 📁 Project Structure

![Project Structure](project-structure.svg)

## 🛠️ Technologies Used

- **Programming Language**: Python 3
- **Data Handling**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Machine Learning**: Scikit-learn, XGBoost
- **Model Evaluation**: Scikit-learn metrics
- **Dashboard** (Optional): Streamlit

**Note**: This project uses only classical Machine Learning (No Deep Learning).

---


---

## 🔍 Methodology

### 1. Data Understanding
- Analyzed engine degradation patterns
- Studied correlation between sensors and engine failure

### 2. Data Preprocessing
- Loaded and cleaned the dataset
- Calculated **Remaining Useful Life (RUL)** for training data
- Handled missing values and outliers

### 3. Feature Engineering
- Created rolling statistics (mean, std, max, min) over last few cycles
- Added lag features
- Removed constant and low-variance sensors
- Feature scaling using StandardScaler

### 4. Machine Learning Models Used

- **Linear Regression** (Baseline)
- **Random Forest Regressor**
- **XGBoost Regressor** ← Best performing model
- **Gradient Boosting Regressor**
- **Support Vector Regressor (SVR)**

### 5. Model Training & Evaluation
- Train-test split on engine units
- Used **RMSE** and **MAE** as primary metrics (critical in aerospace)
- Performed hyperparameter tuning using GridSearchCV
- Cross-validation to ensure robustness

---

## 📈 Results

- **Best Model**: XGBoost Regressor
- **RMSE**: ~XX.XX (replace with your actual result)
- **MAE**: ~XX.XX
- Successfully predicted engine failure trends
- Identified most important sensors affecting engine health

*(Add plots here: Predicted vs Actual RUL, Feature Importance, etc.)*

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/predictive-maintenance-aerospace.git
cd predictive-maintenance-aerospace
