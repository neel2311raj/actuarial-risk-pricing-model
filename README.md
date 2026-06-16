**Actuarial-risk-pricing-model**
An actuarial pricing model using SQL and  Linear Regression.
# Actuarial Risk Analysis & Predictive Pricing Model

A regression-based pricing model estimating health insurance claim costs based on a 1,340-record portfolio.

## 🛠 Tech Stack
* **Data Extraction & EDA:** SQL
* **Predictive Modeling:** Excel (Multivariate Linear Regression, Data Analysis ToolPak)

## 📊 Model Architecture
* **Validation:** 80/20 Train-Test Split
* **Feature Selection:** P-value pruning (Alpha = 0.05)
* **Performance:** R² = 78.09%

### The Pricing Algorithm
Expected Claim Cost is calculated using the following optimized formula. Note the engineered interaction term (`BMI * Smoker`), which isolated catastrophic portfolio risk and drove model accuracy up from 66.1%.


Expected Claim = 
  -$7,277 
  + ($159.00 * BloodPressure) 
  + ($85.50 * BMI) 
  + ($738.00 * Dependents) 
  - ($17,828 * Smoker[1|0]) 
  + ($1,259 * (BMI * Smoker[1|0])) 
  + [Regional Adjustments]
