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

## Key Findings
- **Access to mental health resources** is the strongest predictor (6.2% feature importance)
- **Work location** and **job role** are significant predictors
- **Medium stress category** is most difficult to classify (F1 = 0.32)
- Performance is modest due to substantial class overlap and unmeasured confounders (personality traits, home life factors)

## Methodology
1. **Data preprocessing**: Handled missing values, removed leakage-prone variables (Mental_Health_Condition, Productivity_Change), applied appropriate encoding
2. **Models compared**: XGBoost vs Histogram Gradient Boosting (plus baseline Dummy Classifier)
3. **Evaluation**: Macro-averaged F1 score to ensure balanced performance across all stress levels
4. **Hyperparameter tuning**: RandomizedSearchCV with 30 iterations, 3-fold CV

## Limitations
- Cross-sectional design (cannot establish causation)
- Self-reported data (potential reporting bias)
- Missing key variables (personality traits, objective workplace metrics)
- Dataset from COVID era may not generalize to current remote work contexts

## Author
Poorna Prakash

## License
This project is available for educational purposes.
