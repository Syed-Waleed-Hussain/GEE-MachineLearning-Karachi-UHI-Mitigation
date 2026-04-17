# 🌍 Predictive Modeling and Micro-Climate Mitigation of Urban Heat Islands in Karachi

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-API-success)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn%20%7C%20XGBoost-orange)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-TensorFlow%20%7C%20PyTorch-red)

## 📌 Project Overview
Rapid urbanization and deforestation in Karachi have led to the dangerous escalation of Urban Heat Islands (UHIs). This data science project leverages **Google Earth Engine (GEE)** and **Machine Learning** to create a predictive "Digital Twin" of Karachi's micro-climate. 

We extract spatial environmental indices to predict Land Surface Temperature (LST) and run a **Mitigation Simulation**—hypothetically increasing vegetation density to calculate exact temperature drops.

## 🎯 Key Objectives
- **Data Extraction:** Fetch real-time Landsat 8 satellite imagery using the GEE Python API.
- **Feature Engineering:** Calculate critical spatial indices: NDVI (Vegetation), NDBI (Built-up/Concrete), and NDWI (Water bodies).
- **Predictive Modeling:** Train and evaluate 4 ML models to predict LST.
- **Climate Simulation:** Simulate a 20% increase in urban forestry (NDVI) to measure the localized cooling effect.

## 🛠️ Tech Stack
- **Language:** Python
- **APIs:** Google Earth Engine (`ee`), `geemap`
- **Data Manipulation:** `pandas`, `numpy`, `geopandas`
- **Machine Learning:** `scikit-learn` (Random Forest, SVR), `xgboost`
- **Deep Learning:** `keras` / `pytorch` (MLP)
- **Visualization:** `matplotlib`, `seaborn`, `folium`

## 📂 Project Structure
```text
├── data/                   # Directory for extracted CSV tabular data
├── notebooks/              # Jupyter notebooks for EDA and model training
│   ├── 01_GEE_Data_Extraction.ipynb
│   ├── 02_EDA_and_Preprocessing.ipynb
│   ├── 03_Model_Training_Evaluation.ipynb
│   └── 04_Mitigation_Simulation.ipynb
├── src/                    # Python scripts for custom functions
│   ├── gee_auth.py         # Google Earth Engine authentication
│   └── indices_calc.py     # Functions to calculate NDVI, NDBI, NDWI
├── presentation/           # Project slides and TBW Research Paper (PDF)
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```
## ⚙️ Installation & Setup
Clone the repository:
```git clone [https://github.com/Syed-Waleed-Hussain/Karachi-UHI-Predictive-Modeling.git](https://github.com/your-username/Karachi-UHI-Predictive-Modeling.git)
cd Karachi-UHI-Predictive-Modeling
```
Install required dependencies:
```pip install -r requirements.txt ```
Authenticate Google Earth Engine:
Run the following command in your terminal or Jupyter Notebook to authenticate your Google account with GEE:
```import ee
ee.Authenticate()
ee.Initialize()
```
##  🚀 Methodology & Usage
1. Data Extraction & Preprocessing
   Run 01_GEE_Data_Extraction.ipynb to fetch Landsat 8 bounds over Karachi. The script automatically applies cloud-masking algorithms and exports the pixel data (NDVI, NDBI, NDWI, LST) into a tabular CSV format.
2. Exploratory Data Analysis (EDA)
   Run 02_EDA_and_Preprocessing.ipynb to visualize correlation heatmaps.Expected insight: Strong positive correlation between NDBI (concrete) and LST; strong negative correlation between NDVI (vegetation) and LST.
3. Model Training
   Run 03_Model_Training_Evaluation.ipynb. We implemented and tuned four models:
   Random Forest Regressor
   XGBoostSupport Vector Regression (SVR)
   Multi-Layer Perceptron (MLP)
Evaluation Metrics:Models are evaluated using Root Mean Squared Error ($RMSE$), Mean Absolute Error ($MAE$), and $R^2$ Score.
4. The "What-If" Mitigation Simulation
   Run 04_Mitigation_Simulation.ipynb. This is the core novelty of the project. We take the test dataset, artificially boost the NDVI values by 20%, and use our best-performing model (e.g., XGBoost) to predict the new LST. This simulates a targeted tree-planting campaign in Karachi's hottest zones.

##  📊 Results
(Note: Update this section once your models are fully trained)
Best Performing Model: [e.g., XGBoost with $R^2$ = 0.89]
Simulation Impact: A simulated 20% increase in NDVI resulted in an average local temperature drop of [X.X] °C in highly built-up areas like Saddar and Lyari.

##  👥 Contributors
### Syed Waleed Hussain- GEE Data Pipeline & Modeling
### Abdul Salam - Data Preprocessing & EDA
### Ebrahim Moen - Model Evaluation & Visualizations
### Saniya - Research Documentation & Simulation Analysis
