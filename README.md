# ADS-505 Final Project: Predictive Modeling for Pharmaceutical Sales Performance

## 📖 Project Purpose
This project leverages historical pharmaceutical sales data to develop predictive models that forecast future demand.
Accurate forecasting supports inventory optimization, waste reduction, and production scheduling in a highly seasonal market.
By analyzing six years of sales data across multiple therapeutic categories, this project demonstrates how data science can create measurable value in the pharmaceutical supply chain.

---

## 📦 Dataset
- **Source:** [Pharma Sales Data — Kaggle (Milan Zdravković)](https://www.kaggle.com/datasets/milanzdravkovic/pharma-sales-data?resource=download)  
- **Size:** ~600,000 transaction records (2014–2019)  
- **Variables:** Date/time of sale, drug brand (57 brands), ATC category (8 categories), quantity sold  
- **Format:** Multiple CSVs; can be aggregated hourly/weekly for analysis  
- **Use Case:** Commonly used for time-series forecasting and trend analysis

---

## 🎯 Objectives
- Conduct exploratory analysis to uncover seasonality and category-level trends
- Identify key demand drivers influencing pharmaceutical sales
- Compare multiple forecasting methods:
  - SARIMA (Time-Series Baseline)
  - Random Forest
  - XGBoost
  - Logistic Regression (Surge Detection)
- Translate results into business recommendations for proactive production and inventory management

---

| Model               | Purpose                                                    | Key Strength                                               |
| ------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| SARIMA              | Baseline time-series model capturing trend and seasonality | Interpretable and grounded in classical forecasting theory |
| Random Forest       | Ensemble regression capturing nonlinear interactions       | Strong baseline for predictive accuracy                    |
| XGBoost             | Gradient boosting for improved accuracy and regularization | Highest performing model overall                           |
| Logistic Regression | Binary classifier for surge detection                      | Adds operational early-warning capability                  |

---

## 🌿 Branch Workflow
- `main` → stable, protected branch  
- `kiara`, `saloni`, `kamran` → feature branches; merge into `main` via Pull Requests

---

## 👥 Team Contributions
- **Saloni Barhate** → Data preprocessing/cleaning, EDA, **Linear Regression**, paper & presentation  
- **Kamran Shirazi** → Feature engineering, **Random Forest**, forecasting, paper & presentation  
- **Kiara Paz** → Data preprocessing/cleaning, EDA, **XGBoost**, Time Series Analysis, paper & presentation

---

## 🗂️ Repo Structure
ADS-505-Final-Project-Pharma-Sales-Forecast/
│
├── data/                                
│   ├── raw/                             
│   ├── processed/                       
│   └── train_test/                      
│
├── notebooks/                           
│   ├── Preprocessing-EDA.ipynb          
│   ├── Feature-Engineering+Data-Split.ipynb
│   ├── Modeling-RandomForest+XGBoost.ipynb
│   ├── Time-Series-Analysis.ipynb       
│   └── Logistic-Regression-Surge.ipynb  
│
├── reports/                             
│   ├── figures/                         
│   ├── Technical-Report.pdf             
│   └── Executive-Summary-Presentation.pptx                        
│
├── .gitignore                           
├── requirements.txt                     
├── README.md                            
                            


---
## Results Summary 
| Model               | MAE     | RMSE    | R²                              | Key Insight                                                 |
| ------------------- | ------- | ------- | ------------------------------- | ----------------------------------------------------------- |
| SARIMA              | 1050.59 | 3428.39 | —                               | Established baseline; captures broad seasonal cycles        |
| Random Forest       | 3.70    | 5.77    | 0.939                           | Captured nonlinear relationships and short-term seasonality |
| XGBoost             | 2.14    | 4.02    | 0.971                           | Most accurate; effectively modeled temporal dependencies    |
| Logistic Regression | —       | —       | ROC-AUC = 0.888, PR-AUC = 0.392 | Detected 75% of surge weeks, enabling early demand alerts   |

---

## Github Repo
https://github.com/kpaz357/ADS-505-Final-Project-Pharma-Sales-Forecast 
