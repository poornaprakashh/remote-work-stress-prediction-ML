# remote-work-stress-prediction-ML
Machine learning project predicting high workplace stress using remote work and social factors

# Remote Work Stress Prediction

## Overview
This project uses machine learning to predict stress levels (High, Medium, Low) among remote workers using workplace and behavioral factors.

## Dataset
- Source: Kaggle - Impact of Remote Work on Mental Health
- Size: 5,000 observations, 20 variables
- Target variable: Stress_Level (categorical: High, Medium, Low)

## Repository Structure
```
├── data_exploration.ipynb      # Exploratory data analysis
├── modelling.ipynb             # Model training and evaluation
├── Impact_of_Remote_Work_on_Mental_Health.csv  # Raw data
└── README.md                   # This file
```

## Reproducing the Analysis

### Requirements
```
python >= 3.8
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
```

### Installation
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### Running the Analysis
1. Clone this repository
2. Ensure the data file is in the root directory
3. Run notebooks in order:
   - First: `data_exploration.ipynb`
   - Second: `modelling.ipynb`

### Expected Results
- Final model: XGBoost
- Test accuracy: 34.5%
- F1-macro: 0.345 (105% improvement over baseline)

## Key Findings
- Access to mental health resources is the strongest predictor (6.2% importance)
- Work location and job role are significant predictors
- Medium stress category is most difficult to classify
- Performance is modest due to class overlap and unmeasured confounders

## Author
Poorna Prakash
