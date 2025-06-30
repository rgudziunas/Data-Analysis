# Exploratory Data Analysis & Pre‑processing — Stroke Prediction Dataset

This repository contains a Jupyter notebook (**`Data_Analysis.ipynb`**) that walks through a complete exploratory data analysis (EDA) and data‑cleaning workflow on the open‑source **Stroke Prediction** dataset originally released by *Machine Learning for Healthcare* and hosted on Kaggle.

> **Goal:** understand the factors associated with stroke events and get the data ready for a downstream machine‑learning model.



## 🔍 Notebook Outline

| Section                         | What it does                                                                                                                                                                |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Load data**                | Reads the CSV into a `pandas` DataFrame and prints a head & schema overview.                                                                                                |
| **2. Data cleaning**            | • Replaces `"N/A"` strings with proper `NaN` values<br>• Drops the redundant `id` column<br>• Calculates missing‑value percentages.                                         |
| **3. Exploratory visuals**      | Categorical counts and bar plots for features such as `gender`, `smoking_status`, *etc.*; histograms and KDEs for continuous variables (`age`, `avg_glucose_level`, `bmi`). |
| **4. Feature engineering**      | Encodes categorical variables with **`LabelEncoder`** from `scikit‑learn`.                                                                                                  |
| **5. Next steps (placeholder)** | The notebook stops after EDA + encoding; a follow‑up notebook or script would train ML models.                                                                              |

---

## 🗃️ Dataset

* **Source:** [https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
* **Rows:** \~5 k
* **Target column:** `stroke` (0 = no, 1 = had a stroke)
* **Features:** age, gender, hypertension, heart disease, avg\_glucose\_level, BMI, work type, smoking\_status, *etc.*

The raw CSV is **not committed** to the repo to keep it lightweight. Place it in the project root before running the notebook.

---


## 🚀 Running the notebook

1. Clone this repository

   ```bash
   git clone https://github.com/<your‑username>/<repo‑name>.git
   cd <repo‑name>
   ```
2. (Optional) Create and activate a virtual environment.
3. Install dependencies.
4. Launch Jupyter Lab or Notebook.

   ```bash
   jupyter lab  # or jupyter notebook
   ```
5. Open **`Data_Analysis.ipynb`** and run all cells.

> ℹ️  Some printed messages are in **Lithuanian** (e.g., *eil skaičius*, *trūkstamos reikšmės*) because the project author lives in Vilnius. Feel free to localise or translate as needed.

---

## 📝 Results snapshot

After cleaning, only **`bmi`** retained \~4 % missing values. Basic bar plots revealed class imbalance in **`smoking_status`** and **`work_type`**, while numerical histograms showed a right‑skewed **`avg_glucose_level`**. These insights guided the choice of encoding and potential scaling/transform steps for future modeling.

---


