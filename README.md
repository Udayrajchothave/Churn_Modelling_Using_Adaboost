# Bank Customer Churn Prediction using Optimized AdaBoost

This project implements an optimized **AdaBoost Classifier** to predict customer churn using the `Churn_Modelling.csv` dataset. The model tuning is performed using `GridSearchCV` to optimize the base estimator depth, learning rate, and number of estimators.

## Project Structure
- `Churn_Modelling_Using_Adaboost.ipynb`: Jupyter notebook containing the full data exploration, preprocessing, model tuning, and evaluation pipeline.
- `requirements.txt`: List of dependencies needed to run the project.
- `.gitignore`: Files to ignore in the repository.

## Dataset
The project uses `Churn_Modelling.csv`, which contains customer records from a bank, including features like:
- Credit Score
- Geography & Gender
- Age & Tenure
- Account Balance
- Number of Products
- Activity Status & Estimated Salary
- **Exited** (Target variable: 1 if the customer left the bank, 0 otherwise)

## Model Configuration & Performance
Through 5-fold cross-validation grid search optimization, the optimal parameters found were:
- **Base Estimator**: `DecisionTreeClassifier(max_depth=3)`
- **Learning Rate**: `0.1`
- **Number of Estimators**: `500`

### Evaluation Metrics
- **Best Cross-Validation Accuracy**: `86.06%`
- **Test Set Accuracy**: `86.75%`

#### Classification Report (Test Set):
```text
               precision    recall  f1-score   support

           0       0.88      0.97      0.92      1593
           1       0.79      0.48      0.59       407

    accuracy                           0.87      2000
```

## Installation & Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
   cd YOUR_REPOSITORY_NAME
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook using Jupyter Lab or upload it to Google Colab.
