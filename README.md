# IPL Match Outcome Prediction Project

This project builds a machine learning solution to predict whether a cricket team will win an IPL match based on their performance in the first 10 overs (the powerplay phase).

## Objective
The primary goal is to identify which performance metrics from the first 10 overs are most predictive of overall match victory, providing insights into early match dynamics and their impact on final outcomes.

## Data & Preprocessing
The project uses two datasets:
- **Matches data** (`matches.csv`): Contains match-level information including winner details
- **Deliveries data** (`deliveries.csv`): Ball-by-ball records of all IPL matches

Data preprocessing includes handling missing values (marked as 'NA') and filtering deliveries to the first 10 overs.

## Feature Engineering
Six key features are engineered from first 10 overs data:
1. **Runs scored** - Total runs in first 10 overs
2. **Wickets lost** - Number of dismissals
3. **Boundary count** - Number of 4s and 6s
4. **Dot balls** - Balls on which no runs were scored
5. **Last 2 overs momentum** - Runs scored in overs 9-10 (momentum indicator)
6. **Run rate acceleration** - Difference between runs in overs 6-10 vs overs 1-5

## Methodology
- **EDA**: Correlation analysis, distribution plots, and pairplot visualizations to understand feature relationships
- **Model Training**: Three algorithms are trained and compared:
  - Logistic Regression
  - Decision Tree
  - Random Forest
- **Evaluation**: Models are compared using accuracy, confusion matrices, and classification reports
- **Feature Importance**: The best-performing model's feature importance is visualized to identify the most impactful predictors

## Output
The analysis reveals which early-innings metrics best predict match wins and provides a trained model for making win predictions on new data.
