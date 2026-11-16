# Dairy Farm Cattle Selection — ML Models

ML models to support cattle purchase decisions based on milk yield and milk taste predictions.

## Data
- **Source:** dairy farm internal data
- **Size:** 634 cows (training set), 20 candidate cows (supplier)
- **Features:** breed, pasture type, pedigree, nutrition metrics (energy, fiber, crude protein), milk characteristics

## Workflow
- Data preprocessing: handling missing values, duplicate removal, type conversion
- EDA: distribution analysis, correlation analysis (Phik)
- Feature engineering: adding squared energy feature, fiber binarization, merging pedigree data
- Three linear regression models for milk yield prediction, best model selection (R²=0.85)
- Logistic regression model for milk taste classification
- Classification threshold optimization for the business objective (precision maximization)
- Milk yield and taste prediction for 20 candidate cows

## Key Findings
- **Yield model:** R²=0.85; iterative improvement through feature engineering raised quality from 0.82 to 0.85; 17 out of 20 supplier cows meet the 6,000 kg/year threshold
- **Taste model:** after threshold optimization to 0.795, precision=0.93 — the model approves a cow only when highly confident in milk quality
- **Result:** out of 20 candidates, only 2 cows meet both criteria (yield ≥6,000 kg + good taste)
- **Limitations:** small training set limits classification quality; final purchase decisions should also consider animal cost and health history

## Tech Stack
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-lightgrey)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-lightgrey)
![Matplotlib](https://img.shields.io/badge/Matplotlib-lightgrey)
![Seaborn](https://img.shields.io/badge/Seaborn-lightgrey)
![Phik](https://img.shields.io/badge/Phik-lightgrey)

## Repository Structure
```
├── dairy_farm_ml_models.ipynb  # main notebook
└── README.md
```
