# NBA Game Outcome Prediction Model

This project predicts NBA game outcomes using machine learning techniques. It involves data cleaning, feature engineering, model training, evaluation, and finally, making predictions on upcoming games.

## Modeling Approach

1. **Data Cleaning**:  
   - Missing values handled via imputation or removal  
   - Data types corrected for consistency  
   - Outliers addressed based on domain-specific knowledge  

2. **Feature Engineering**:  
   - Rolling averages for recent team performances  
   - Rest day calculations  
   - Win/loss streak features, home/away splits  

3. **Model Selection & Training**:  
   - Example models: Logistic Regression, Random Forest, XGBoost  
   - Hyperparameter tuning via Grid Search or Random Search  
   - Cross-validation for robust model performance estimation  

4. **Evaluation**:  
   - Key metrics: Accuracy, Precision, Recall, F1 score  
   - Confusion matrix analysis  
   - Feature importance inspection (particularly for tree-based models)  

5. **Prediction**:  
   - Given matchup data (e.g., Team A vs. Team B on a certain date), the model outputs the predicted winner.
