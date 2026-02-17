# Remote Work Stress Prediction

## Overview
This project uses machine learning to predict stress levels (High, Medium, Low) among remote workers using workplace and behavioral factors.

## Dataset
- Source: Kaggle - Impact of Remote Work on Mental Health
- Size: 5,000 observations, 20 variables
- Target variable: Stress_Level (categorical: High, Medium, Low)

## Repository Structure
```
├── notebook/
│   ├── data_exploration.ipynb   # Exploratory data analysis
│   └── modelling.ipynb          # Model training and evaluation
├── data/
│   └── Impact_of_Remote_Work_on_Mental_Health.csv  # Raw data
├── .gitignore
└── README.md                    # This file
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
1. Clone this repository:
```bash
   git clone https://github.com/poornaprakashh/remote-work-stress-prediction-ML.git
   cd remote-work-stress-prediction-ML
```

2. Navigate to the notebook directory:
```bash
   cd notebook
```

3. The data file is located in the `../data/` directory (one level up from notebooks). The notebooks are already configured to read from this location using the relative path `../data/Impact_of_Remote_Work_on_Mental_Health.csv`.

4. Run notebooks in order:
   - **First**: `data_exploration.ipynb` - Performs exploratory data analysis
   - **Second**: `modelling.ipynb` - Trains models and evaluates performance

### Expected Results
- **Final model**: XGBoost (tuned with RandomizedSearchCV)
- **Test accuracy**: 34.5%
- **F1-macro**: 0.345 (105% improvement over baseline)
- **Cross-validation**: 5-fold stratified CV with F1-macro as metric

## Author
Poorna Prakash

## License
This project is available for educational purposes.
