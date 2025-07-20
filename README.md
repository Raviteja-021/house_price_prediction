# 🏠 Housing Price Prediction using Linear Regression

This project uses **Linear Regression** to predict house prices based on various features such as area, number of bedrooms, bathrooms, and more. The goal is to understand the relationship between housing features and price, and build a predictive model using basic regression techniques.

---

## 📁 Dataset

- **File:** `Housing.csv`
- **Entries:** 545 rows × 13 columns
- **Target Variable:** `price`
- **Features:**
  - `area`: Square footage of the house
  - `bedrooms`, `bathrooms`, `stories`
  - `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`: Binary categorical features
  - `parking`
  - `prefarea`: Preferred location (yes/no)
  - `furnishingstatus`: Furnishing type

---

## 🔍 Workflow

### 1. **Library Imports**
- `pandas`, `numpy` for data handling
- `matplotlib`, `seaborn` for visualization
- `scikit-learn` for model building and evaluation

### 2. **Exploratory Data Analysis**
- Checked for missing values
- Visualized data using pair plots, correlation heatmaps, and box plots
- Identified and removed outliers using the **IQR method** on `price` and `area`

### 3. **Data Preparation**
- Selected numeric features: `area`, `bedrooms`, `bathrooms`, `price`
- Filtered dataset to remove extreme values
- Final dataset shape: **(517, 4)**

### 4. **Modeling**
- Used `train_test_split` with 80% training, 20% testing
- Built a `LinearRegression` model with:
  - Inputs: `area`, `bedrooms`, `bathrooms`
  - Target: `price`
- Fitted and evaluated the model

### 5. **Evaluation**
- Metrics used:
  - **R² Score**: ~0.516
  - **Mean Squared Error (MSE)**
- Plots:
  - Actual vs Predicted scatter plot
  - Regression line with Seaborn

### 6. **Model Coefficients**
- Coefficients show:
  - ~₹407 increase per square foot
  - ~₹4.08 lakh increase per bedroom
  - ~₹10.2 lakh increase per bathroom

---

## 📊 Results Summary

| Metric | Value |
|--------|-------|
| R² Score | ~0.516 |
| Model | Linear Regression |
| Features Used | `area`, `bedrooms`, `bathrooms` |

---

## 🛠️ Installation & Setup

### ✅ Requirements

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
