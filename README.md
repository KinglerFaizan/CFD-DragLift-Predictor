# ✈️ CFD Drag & Lift Prediction Using Random Forest

This project uses machine learning to predict aerodynamic drag (`coefficientDrag`) and lift (`coefficientLift`) coefficients for airfoil surfaces, based on computational fluid dynamics (CFD) simulation data.

### 📌 Objective
To develop a data-driven regression model capable of estimating drag and lift from surface coefficient data using the Random Forest algorithm.

---

## 📂 Dataset Overview

- **File:** `combinedAirfoilDataLabeled.csv`
- **Shape:** 867,098 rows × 71 columns
- **Features:** Surface pressure coefficients (`upperSurfaceCoeff1` to `upperSurfaceCoeff70`)
- **Targets:** `coefficientDrag`, `coefficientLift`

---

## 🔧 Methodology

- **Preprocessing:**
  - Dropped missing values
  - Standardized features
  - Downsampled for memory efficiency
- **Model:**
  - `RandomForestRegressor` (scikit-learn)
  - Trained on a 10,000-sample subset
- **Prediction:**
  - Tested on the full test set
- **Evaluation:**
  - Used `mean_absolute_error` and scatter plots

---

## 📈 Visualizations

- Distribution of target values (Cd & Cl)
- Actual vs Predicted plots
- Feature importances (top coefficients)

---

## 🛠️ Tech Stack

- Python 3.x
- pandas, numpy
- scikit-learn
- seaborn, matplotlib

---

## 🚀 How to Run

1. Clone this repository
2. Place the dataset in the `/data` folder
3. Launch the Jupyter notebook `notebook/CFD.ipynb`
4. Execute all cells to preprocess data, train model, and visualize results

---

## 🧪 Future Enhancements

- Batch-wise training on full dataset
- Use `XGBoost` or `GradientBoostingRegressor`
- Hyperparameter tuning (`max_depth`, `max_features`, etc.)
- Cloud deployment (optional)

---


