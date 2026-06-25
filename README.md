# California Property Close Price Prediction

## 📌 Project Overview
This repository contains a machine learning workflow developed to predict the historical close price (final sales price) of single residential properties across California. [cite_start]Sourced from the California Regional Multiple Listing Service (CRMLS), the model leverages structural and geographic characteristics of properties to estimate valuation accuracy at the time of query[cite: 14, 16].

### Core Objectives
* [cite_start]Filter observations exclusively to `Property Type="Residential"` and `Property Sub Type="Single Family Residence"`[cite: 13].
* [cite_start]Clean, preprocess, and engineer complex feature layers (including geometric school district joins) to optimize model accuracy[cite: 20, 76].
* [cite_start]Evaluate multiple algorithms (Linear Regression, Tree Ensembles, and Gradient Boosting) to deliver a high-performing production model[cite: 23].

---

## 📂 Repository Structure
```text
├── notebooks/
│   ├── 01_exploration.ipynb       # Exploratory data analysis (EDA) & baseline plots
│   ├── 02_preprocessing.ipynb     # Missing value handling & data windows
│   ├── 03_baseline_model.ipynb    # Initial Linear Regression training
│   ├── 04_model_comparison.ipynb  # Decision Tree & Random Forest comparison
│   ├── 05_advanced_models.ipynb   # Gradient Boosting (XGBoost/LightGBM) tuning
│   └── 06_evaluation.ipynb        # Final model metrics (R², MAPE, MdAPE)
├── scripts/
│   ├── data_processing.py         # Modular cleaning and encoding scripts
│   ├── model_training.py          # Finalized machine learning training pipeline
│   └── prediction.py              # Inferences execution script
├── data/                          # Created locally (Hidden from GitHub via .gitignore)
│   └── raw/                       # Drop downloaded CRMLSSold files here
├── app.py                         # Optional Streamlit interface for property predictions
├── .gitignore                     # Explicitly configured to ignore raw CSV/source files
├── requirements.txt               # Project Python dependencies
└── README.md                      # Project documentation


---

## 🛠️ Setup & Installation

### 1. Clone the Repository
```bash
git clone [https://github.com/nishitameda-dev/IDX-Exchange.git](https://github.com/nishitameda-dev/IDX-Exchange.git)
cd IDX-Exchange


pip install -r requirements.txt
