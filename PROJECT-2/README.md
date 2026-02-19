# 🏠 House Price Prediction — Linear Regression

A beginner-friendly Machine Learning project that predicts California house prices using **Linear Regression** and the built-in `sklearn` California Housing dataset.

---

## 📌 Project Overview

| Item | Detail |
|------|--------|
| **Type** | Supervised Learning — Regression |
| **Algorithm** | Linear Regression |
| **Dataset** | California Housing (`sklearn.datasets`) |
| **Goal** | Predict median house value based on neighborhood features |
| **Environment** | Google Colab / Jupyter Notebook |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| `NumPy` | Numerical computations |
| `Pandas` | Data loading & manipulation |
| `Matplotlib` | Data visualization |
| `Scikit-Learn` | ML model, dataset & evaluation metrics |

---

## 📂 Dataset — California Housing

Loaded directly from `sklearn` — **no download needed**.

```python
from sklearn.datasets import fetch_california_housing
data = fetch_california_housing()
```

| Feature | Description |
|---------|-------------|
| `MedInc` | Median income in block group |
| `HouseAge` | Median house age |
| `AveRooms` | Average number of rooms |
| `AveBedrms` | Average number of bedrooms |
| `Population` | Block group population |
| `AveOccup` | Average house occupancy |
| `Latitude` | Geographic latitude |
| `Longitude` | Geographic longitude |
| `Price` *(target)* | Median house value (in $100,000s) |

- **Rows:** 20,640 &nbsp;|&nbsp; **Columns:** 9 &nbsp;|&nbsp; **Missing Values:** None ✅

---

## 🔄 Project Workflow

```
Step 1  → Import Libraries
Step 2  → Load Dataset (fetch_california_housing)
Step 3  → Data Understanding  (shape, dtypes, describe)
Step 4  → Check Missing Values
Step 5  → Feature / Target Split  (X and y)
Step 6  → Train-Test Split  (80% train / 20% test)
Step 7  → Train Linear Regression Model
Step 8  → Make Predictions on Test Set
Step 9  → Evaluate Model  (RMSE + R²)
Step 10 → Visualization — Actual vs Predicted scatter plot
Step 11 → Residual Plot  (error analysis)
Step 12 → Feature Importance  (regression coefficients)
Step 13 → Improvement via Log Transform  (feature engineering)
Step 14 → Save Predictions to CSV
```

---

## 📊 Model Results

| Metric | Baseline Model | After Log Transform |
|--------|:--------------:|:-------------------:|
| **RMSE** | 0.7456 | 0.2244 |
| **R² Score** | 0.5758 | 0.6006 |

> 📉 **RMSE** — Root Mean Square Error. Lower = better.  
> 📈 **R²** — How well the model explains variance. Closer to 1.0 = better.

---

## 🔍 Feature Importance (Coefficients)

| Feature | Coefficient | Effect on Price |
|---------|:-----------:|----------------|
| `AveBedrms` | +0.783 | ⬆️ Increases |
| `MedInc` | +0.449 | ⬆️ Increases |
| `HouseAge` | +0.010 | ⬆️ Increases |
| `Population` | −0.000002 | ⬇️ Decreases |
| `AveOccup` | −0.004 | ⬇️ Decreases |
| `AveRooms` | −0.123 | ⬇️ Decreases |
| `Latitude` | −0.420 | ⬇️ Decreases |
| `Longitude` | −0.434 | ⬇️ Decreases |

> A **positive** coefficient means the feature pushes the predicted price up; a **negative** coefficient pulls it down.

---

## 🚀 How to Run

### Option 1 — Google Colab *(recommended)*
1. Upload `Project_2__HPR_.ipynb` to [Google Colab](https://colab.research.google.com/)
2. Click **Runtime → Run All**

### Option 2 — Local Jupyter
```bash
# Install dependencies
pip install numpy pandas matplotlib scikit-learn

# Launch notebook
jupyter notebook Project_2__HPR_.ipynb
```

---

## 📁 Files

```
📦 Project
 ┣ 📓 Project_2__HPR_.ipynb        # Main notebook
 ┗ 📄 house_price_prediction.csv   # Saved prediction results (Actual vs Predicted)
```

---

## 🧠 Key Concepts Covered

- Loading a built-in `sklearn` dataset
- Exploratory Data Analysis (EDA)
- Train / Test split with `random_state` for reproducibility
- Training and evaluating a Linear Regression model
- Interpreting RMSE and R² metrics
- Scatter plot & residual plot visualization
- Feature engineering with log transformation (`np.log1p`)
- Exporting results to CSV

---

## 👤 Author

**BUBAI DE**
- GitHub: [@Developer-Bubai](https://github.com/Developer-Bubai)
- LinkedIn: [Developer-Bubai](www.linkedin.com/in/bubai-de-0599093b1)

  
## 📄 License

This project is open source and available under the [MIT License](LICENSE).
