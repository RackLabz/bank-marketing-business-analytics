# Bank Marketing Campaign Response Prediction

## Business Context
Direct marketing campaigns are expensive and often inefficient when applied uniformly across all customers.  
The goal of this project is to predict which clients are most likely to subscribe to a term deposit, allowing a bank to focus outreach on high-probability customers and improve campaign efficiency.

This project is framed as a **business analytics case study**, not just a modeling exercise. Emphasis is placed on evaluation, decision trade-offs, and practical use of model outputs.

---

## Dataset
- **Source:** UCI Machine Learning Repository – Bank Marketing Dataset  
  https://archive.ics.uci.edu/dataset/222/bank+marketing
- **Size:** 41,188 records
- **Features:** Client demographics, campaign details, and macro-economic indicators
- **Target:**  
  `y`: whether the client subscribed to a term deposit (yes/no)

The dataset reflects real campaign data, including class imbalance and mixed data types.

---

## Analytical Workflow

### 1. Data Audit
- Checked for duplicates, missing values, and inconsistent data types
- Standardized column names
- Converted the target variable into a binary numerical format

### 2. Exploratory Data Analysis
- Examined subscription rates across customer segments
- Analyzed campaign variables and economic indicators
- Compared numeric feature distributions by outcome to identify patterns

### 3. Preprocessing
- Built preprocessing pipelines using scikit-learn to avoid data leakage
- Applied:
  - One-hot encoding for categorical variables
  - Standardization for numeric variables
- All preprocessing was performed inside the modeling pipeline

### 4. Modeling
Models evaluated include:
- Dummy baseline classifier
- Regularized Logistic Regression
- Random Forest
- Gradient Boosting

Logistic Regression was used as an interpretable baseline, while tree-based models captured non-linear relationships.

### 5. Evaluation
- Stratified train/validation/test split
- Primary metrics:
  - ROC-AUC
  - Precision-Recall AUC (PR-AUC), due to class imbalance
- Learning curves were used to assess overfitting and underfitting
- Cross-validation supported model comparison

### 6. Threshold Selection
Instead of relying on a default probability threshold, different thresholds were evaluated to balance recall and precision based on campaign objectives. This demonstrates how model outputs can be aligned with real operational constraints.

---

## Results Summary
- All trained models outperformed the baseline classifier
- Tree-based models achieved the strongest predictive performance
- Learning curves indicated controlled model complexity
- Targeting the highest-probability segment produced a clear lift over the baseline subscription rate

(Exact metrics and plots are available in the notebook.)

---

## Key Insights
- Outcomes of previous campaigns strongly influence future subscription likelihood
- Contact method and campaign context materially affect response rates
- Model performance alone is insufficient; threshold choice significantly impacts business outcomes
- The final model can be used to generate ranked customer lists for targeted outreach

---

## Reproducibility
To reproduce this project:
1. Clone the repository:
   ```bash
   git clone https://github.com/RackLabz/bank-marketing-business-analytics.git
   cd bank-marketing-business-analytics

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Author
Ugwuoke Shedrack Chinonso  
GitHub: https://github.com/RackLabz  
LinkedIn: https://www.linkedin.com/in/shedrack-chinonso-69058219a
