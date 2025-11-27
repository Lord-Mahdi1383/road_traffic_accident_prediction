# Road Traffic Accident Severity Prediction


## 📌 Overview
This project builds a Machine Learning model to predict the severity of road traffic accidents (e.g., Slight Injury, Serious Injury, Fatal Injury). Using the RTA (Road Traffic Accident) dataset.  
the project involves Exploratory Data Analysis (EDA), data cleaning, feature engineering, and model training using CatBoost.


## ⚙️ Project Workflow
  1. **Data Cleaning**
     - filling columns with high missing values with 'unknown' to avoid ruining the data
     - filling columns with less missing values with most frequent value (mode)
  3. **Feature Engineering**
     - time extraction: converted accident time to hour of day
     - created a new column (is weekend) to find accident patterns on saturdays/sundays
     - dangerous driving combination:
       - Darkness + Wet roads
  5. **EDA**
     - severity distribution on pie chart
     - impact of road surface, weather and lighting on severity
     - histogram and heatmap of day of week and hour of day
     - driver and vehicle related plots
     - causes of accident on a barplot
  7. **Preprocessing**
     - applied 'LabelEncoder' to convert categorical data into numerical for correlation analysis
     - splitting the data into 30% test and 70% train
  9. **Model Training**
      - Algorithm: CatBoostClassifier
      - imbalance handing using auto_class_weights='Balanced' to give more weight to minority classes
      - hyperparameter tuning using GridSearchCV to optimize:
        - iterration, learning rate, depth and l2 leaf reg

## 🛠️ Challanges
### High number of features in the dataset
  - one method is to combine 2 features into one important and critical feature
  - or we can just use algorithms like catboost to handle these
### imbalaced dataset
  - we can use oversampling methods like smote but that doesn't perform well because of creating noisy dataset in fact it even lowered the model recall and f1 score
  - another method is weighted training which does actually increase the model performace a little

## 🚀 How to Run
### Clone the repository:
```bash
git clone https://github.com/Lord-Mahdi1383/road_traffic_accident_prediction
cd road_traffic_accident_prediction
```

### Install Dependencies:
```bash
pip install -r Requirements.txt
```







