# Loan Default Predict (Coursera Challenge - Top 1%)

Achieved 99th percentile in the [Data Science Coding Challenge: Loan Default Prediction](https://www.coursera.org/projects/data-science-coding-challenge-loan-default-prediction)

Link to project coding file: [LoanDefaultPrediction.ipynb](https://sharedczzkddsj.labs.coursera.org/notebooks/LoanDefaultPrediction.ipynb)

This project built an ensemble model to predict loan default probability using real-world historical customers and financial features.

## Final Results

| Dataset | ROC-AUC | Average Precision | Brier Score |
|:--|--:|--:|--:|
| Validation | 0.7508 | 0.3180 | 0.0916 |
| **Test (Unseen)** | **0.7608** | **0.320 (approx)** | **0.091 (approx)** |

<img width="846" height="616" alt="Image" src="https://github.com/user-attachments/assets/1e3569f4-8d3c-44ff-b7be-8bf9a439eb09" />

- Rank: 99th percentile (Top 1%)
- Participants: 6,212
- Model type: Ensemble (Neural Network + LightGBM + XGBoost)

<img width="472" height="433" alt="Image" src="https://github.com/user-attachments/assets/7e93aa10-fc72-47f4-8a6a-fa9acdff0da7" />

## Key Takeaways
- Ensemble blending improved both AUC and probability calibration.
- Neural networks captured a smooth nonlinear relationship, while tree models stabilized performance.
- The model generalized well, improving ROC-AUC on the unseen test set.

## Visual Insights
- Calibration Curve - Neural Network Model

<img width="846" height="545" alt="Image" src="https://github.com/user-attachments/assets/78f4345c-9cfe-4489-bab3-1785548938fe" />
  
- Precision-Recall Curve - Neural Network Model
<img width="846" height="545" alt="Image" src="https://github.com/user-attachments/assets/70c7bf4f-471f-45a7-adf5-b9b8d30c6fdc" />

- Precision and Recall vs. Threshold - Neural Network Model

  <img width="846" height="545" alt="Image" src="https://github.com/user-attachments/assets/ee2f70e6-3ab2-4685-a45e-a20e2275c635" />

### SHAP Analysis
- Linear Logistic Regression Model
<img width="789" height="940" alt="Image" src="https://github.com/user-attachments/assets/1951d182-e162-440d-a5f4-11a120e85843" />

```
SHAP shows that the most influential features driving loan default predictions are:
- InterestRate: Higher interest rates significantly increase the likelihood of loan default. This is matched by the high positive coefficient of 0.4979 for InterestRate in the logistic regression model, indicating that as interest rates rise, so does the risk of default. High rate often leads to higher monthly payments, which can strain borrowers' finances and increase default risk.
- DebtToIncomeRatio: A higher debt-to-income ratio indicates that a borrower has a higher level of debt relative to their income, which can increase the risk of default. The coefficient for DebtToIncomeRatio in the logistic regression model is also positive, suggesting that as this ratio increases, the likelihood of default increases.
- LowCreditFlag: Borrowers with low credit scores are at a significantly higher risk of defaulting on their loans. The logistic regression model's positive coefficient of 0.4991 for LowCreditFlag corroborates this finding, indicating that lower creditworthiness is a strong predictor of default.
- EmploymentStability: Greater employment stability is associated with a lower risk of loan default. The negative coefficient of -0.3067 for EmploymentStability in the logistic regression model supports this, suggesting that borrowers with stable employment are less likely to default.
- AgeGroup_25-34: Younger borrowers in the 25-34 age group have a higher likelihood of defaulting on their loans. This is consistent with the positive coefficient of 0.6799 for AgeGroup_25-34 in the logistic regression model, indicating that younger age is a risk factor for default.
- CreditScorePerAge: A lower credit score relative to age increases the risk of default. The positive coefficient of 0.2622 for CreditScorePerAge in the logistic regression model supports this, indicating that borrowers with low credit scores relative to their age are more likely to default.
- CreditLinePerAge: A higher number of credit lines relative to age increases default risk. The positive coefficient of 0.2435 for CreditLinePerAge in the logistic regression model supports this, indicating that borrowers with more debt per credit line are at higher risk of default.
- EmploymentType_Unemployed: Unemployed borrowers are at a significantly higher risk of defaulting on their loans. The logistic regression model's positive coefficient of 0.4457 for EmploymentType_Unemployed corroborates this finding, indicating that unemployment is a strong predictor of default.
- AgeGroup_18-24: The youngest borrowers in the 18-24 age group have the highest likelihood of defaulting on their loans. This is consistent with the positive coefficient of 0.7516 for AgeGroup_18-24 in the logistic regression model, indicating that being in this youngest age group is a significant risk factor for default.
```

- XGBoost Model

<img width="787" height="940" alt="Image" src="https://github.com/user-attachments/assets/51f28db7-11b4-4d59-81aa-956b94e08b60" />

- LightGBM Model
- 
<img width="787" height="940" alt="image" src="https://github.com/user-attachments/assets/b9e00516-863f-4d21-a9f0-5a2202011fc6" />

## Contact

Thanh Xuyen, Nguyen

LinkedIn: [xuyen-thanh-nguyen-0518](https://www.linkedin.com/in/xuyen-thanh-nguyen-0518/)

Email: thanhxuyen.nguyen@outlook.com
