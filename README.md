# California Property Close Price Prediction

IDX Exchange — Data Science Internship | Intern: Nishitameda | Data Source: CRMLS

## 📌 Project Overview
This repository contains a machine learning workflow developed to predict the historical close price (final sales price) of single residential properties across California. Sourced from the California Regional Multiple Listing Service (CRMLS), the model leverages structural and geographic characteristics of properties to estimate valuation accuracy at the time of query.

### Core Objectives
* Filter observations exclusively to `Property Type="Residential"` and `Property Sub Type="Single Family Residence"`.
* Clean, preprocess, and engineer complex feature layers (including geometric school district joins) to optimize model accuracy.
* Evaluate multiple algorithms (Linear Regression, Tree Ensembles, and Gradient Boosting) to deliver a high-performing production model.

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
🛠️ Setup & Installation1. Clone the RepositoryBashgit clone [https://github.com/nishitameda-dev/IDX-Exchange.git](https://github.com/nishitameda-dev/IDX-Exchange.git)
cd IDX-Exchange
2. Install DependenciesBashpip install pandas numpy scikit-learn xgboost lightgbm matplotlib seaborn jupyter streamlit
3. Secure Dataset Connection (Crucial)Per internship security guidelines, raw data files are strictly excluded from GitHub. Follow these steps to fetch the source files into your local directory:Open FileZilla Client.Connect to the data server using the credentials below:Host: 199.250.207.194Username: data@idxexchange.comPassword: Real_estate123$ (Type manually; do not copy/paste)Port: 21Navigate to the remote path raw/California and copy a minimum of 6 months of files starting with the prefix CRMLSSold.Create a folder named data/raw/ in the root of your local workspace and place the downloaded copies inside.(Optional) Download Trestle Property MetaData.pdf from the remote resources directory to evaluate explicit field descriptions.⚙️ Data Preprocessing & ValidationTarget Variable: ClosePrice is the targeted value the model is trained to predict.Feature Engineering: Features include baseline structural variables (LivingArea, Bedrooms, Bathrooms, LotSize) along with custom metrics (bed/bath ratio, property age) and geometric coordinates joined against the CA School District Areas 2024-25 boundaries.Data Validation Window: The testing split utilizes the most recent month of available data. The preceding $X$ months are set aside as the variable training scope to optimize historical temporal thresholds.🚀 How to Run the WorkRun the Data PipelinesTo execute the modular data preprocessing scripts and initiate model training routines:Bashpython scripts/data_processing.py
python scripts/model_training.py
Run the Prediction AppTo launch the interactive frontend dashboard to query customized property pricing assumptions:Bashstreamlit run app.py
📊 Models Tested & EvaluationThe project records progressive iterations to identify optimal close-price predictions. Performance will be evaluated across three core metrics: $R^2$ (variance explanation), MAPE (Mean Absolute Percentage Error), and MdAPE (Median Absolute Percentage Error).Model IterationKey Evaluated FeaturesTarget Metrics (R2, MAPE, MdAPE)StatusLinear Regression BaselineBaseline structural variables[TBD Week 4]PendingTree Ensembles (RF/DT)Baseline structural variables[TBD Week 5]PendingAdvanced Gradient BoostingStructural + CA School Districts Layer[TBD Week 7]Pending📅 12-Week TimelineWeekFocusDeliverable / MilestoneWeek 1Setup, FTP access, dataset reviewRepository configuration, .gitignore validationWeek 2Exploratory Data Analysis01_exploration.ipynb baseline plotsWeek 3Data Preprocessing02_preprocessing.ipynb missing values & trackingWeek 4Baseline Model03_baseline_model.ipynb Linear Regression trainingWeek 5Additional Models04_model_comparison.ipynb Decision Tree & Random ForestWeek 6Feature EngineeringGeometric join against CA School District layersWeek 7Advanced Models05_advanced_models.ipynb XGBoost / LightGBM tuningWeek 8Evaluation Expansion06_evaluation.ipynb full MAPE/MdAPE error expansionWeek 9Simple Prediction AppInteractive local frontend execution (app.py)Week 10DocumentationComplete finalize routine on README.md and script logsWeek 11Practice PresentationSummary slide deck generationWeek 12Final Team Presentation & HandoffLive Zoom presentation to stakeholder Aidan👥 Contributors & StakeholdersNishitameda - Data Science InternAidan - Project Stakeholder / Presentation LeadTeammate Collaborators - Peer Reviewers

