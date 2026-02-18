# 🚢 Titanic — Exploratory Data Analysis (EDA)

A beginner-friendly data analysis project exploring the Titanic passenger dataset using Python. This project covers the full EDA workflow: loading data, understanding its structure, handling missing values, running statistical analysis, and visualizing key patterns.

---

## 📌 Project Overview

| Detail | Info |
|---|---|
| **Dataset** | [Titanic — Machine Learning from Disaster](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv) |
| **Records** | 891 passengers, 12 features |
| **Tools** | Python, Pandas, Matplotlib |
| **Environment** | Google Colab |

---

## 🎯 Objectives

- Load and inspect a real-world dataset
- Understand data types, shape, and structure
- Identify and handle missing values
- Perform simple statistical analysis
- Visualize survival patterns across passenger demographics

---

## 🗂️ Dataset Features

| Column | Description |
|---|---|
| `PassengerId` | Unique identifier for each passenger |
| `Survived` | Survival status (0 = No, 1 = Yes) |
| `Pclass` | Passenger class (1st, 2nd, 3rd) |
| `Name` | Passenger name |
| `Sex` | Gender |
| `Age` | Age in years |
| `SibSp` | # of siblings/spouses aboard |
| `Parch` | # of parents/children aboard |
| `Ticket` | Ticket number |
| `Fare` | Passenger fare |
| `Cabin` | Cabin number |
| `Embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## 🔍 EDA Steps

### Step 1 — Import Libraries
```python
import pandas as pd
import matplotlib.pyplot as plt
```

### Step 2 — Load Dataset
```python
url = "https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv"
df = pd.read_csv(url)
```

### Step 3 — Understand the Data
- Inspected shape: **891 rows × 12 columns**
- Reviewed column data types using `df.info()`
- Generated descriptive statistics using `df.describe()`

### Step 4 — Handle Missing Values

| Column | Missing Values | Strategy |
|---|---|---|
| `Age` | 177 | Filled with **mean age** (~29.7) |
| `Cabin` | 687 | Dropped (too sparse) |
| `Embarked` | 2 | Filled with **mode** (Southampton) |

### Step 5 — Simple Analysis
- Survival counts and rates
- Survival breakdown by gender and passenger class
- Age and fare distribution analysis

### Step 6 — Visualizations
- Bar charts for survival counts and gender-based survival
- Histograms for age and fare distributions
- Class-wise survival comparison

---

## 📊 Key Findings

- **Overall survival rate:** ~38.4% of passengers survived
- **Gender gap:** Female passengers had a significantly higher survival rate than male passengers
- **Class effect:** 1st class passengers survived at a much higher rate than 3rd class
- **Age:** Missing for ~20% of passengers; average age was ~30 years
- **Fare spread:** Highly skewed — most passengers paid low fares, but a few paid over £500

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data loading, cleaning, and analysis
- **Matplotlib** — data visualization
- **Google Colab** — development environment

---

## 🚀 Getting Started

### Option 1 — Run in Google Colab
Click the badge or open the `.ipynb` file directly in [Google Colab](https://colab.research.google.com/).

### Option 2 — Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/titanic-eda.git
   cd titanic-eda
   ```

2. Install dependencies:
   ```bash
   pip install pandas matplotlib
   ```

3. Launch Jupyter:
   ```bash
   jupyter notebook Project_1__EDA_.ipynb
   ```

---

## 📁 Project Structure

```
titanic-eda/
│
├── Project_1__EDA_.ipynb   # Main notebook with full EDA
└── README.md               # Project documentation
```

---

## 🌱 Future Improvements

- [ ] Feature engineering (e.g., family size, title extraction from name)
- [ ] Correlation heatmap
- [ ] Predictive modeling (Logistic Regression, Decision Tree)
- [ ] Interactive visualizations with Plotly or Seaborn

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Built as part of a data science learning journey. Dataset sourced from [Data Science Dojo](https://github.com/dsrscientist/dataset1).*
