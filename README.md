# Customer_Insurance_Predictions_S11

## Project Description
The Sure Tomorrow insurance company aims to leverage machine learning to enhance its operations. This project focuses on evaluating the feasibility of solving multiple tasks using predictive models.

### Tasks:
1. **Customer Similarity Identification**  
   - Identify customers who are similar to a given customer to assist marketing efforts.
   
2. **Insurance Benefit Prediction**  
   - Develop a classification model to predict whether a new customer is likely to receive an insurance benefit.
   - Compare the trained model's performance against a dummy model to assess effectiveness.
   
3. **Benefit Count Prediction**  
   - Use a linear regression model to predict the number of insurance benefits a customer is likely to receive.
   
4. **Data Protection**  
   - Implement a data obfuscation algorithm to protect personal information while maintaining model accuracy.
   - Ensure that the transformation makes data recovery difficult if accessed by unauthorized parties.

## Data Description
- The dataset is stored in `/datasets/insurance_us.csv`.
- **Features:**
  - Insured person's gender
  - Age
  - Salary
  - Number of family members
- **Target Variable:**
  - Number of insurance benefits received by an insured person over the past five years.

## Data Preparation
### Data Exploration
- The dataset was loaded and inspected for structure and content.
- Missing values and anomalies were identified and addressed.

### Data Quality Verification
- Checked for missing data, extreme values, and inconsistencies.

## Model Development
### Task 1: Customer Similarity
- Feature selection and preprocessing were performed.
- A similarity metric was chosen and applied to identify comparable customers.

### Task 2: Binary Classification Model
- A classification model was trained to predict insurance benefit eligibility.
- Performance was compared against a dummy model to determine effectiveness.

### Task 3: Regression Model for Benefit Prediction
- A linear regression model was implemented to estimate the number of benefits received.
- Model accuracy was evaluated using standard regression metrics.

### Task 4: Data Obfuscation
- A transformation algorithm was developed to mask personal data.
- The impact on model accuracy was assessed to ensure usability.

## Evaluation and Findings
- Each model was validated using appropriate performance metrics.
- Comparisons between models were conducted to determine effectiveness.
- The success of the data obfuscation technique was analyzed.

## Conclusion
- Machine learning was successfully applied to improve predictions for Sure Tomorrow insurance.
- The feasibility of customer similarity detection and benefit prediction was demonstrated.
- Data security measures were implemented without compromising model performance.
