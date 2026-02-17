# Bank Marketing: Business Analytics & Machine Learning

Predict whether a customer will subscribe to a term deposit using historical bank marketing campaign data.
This project demonstrates an end-to-end workflow from data preparation to evaluation and interpretation, with a business lens.

## Project Highlights
- Reproducible preprocessing and modeling pipeline (no data leakage)
- Model comparison using ROC-AUC and PR-AUC
- Final evaluation on a held-out test set
- Feature driver analysis via permutation importance

## Dataset
- Source: UCI Bank Marketing Dataset
- Rows: ~41,000 records
- Target: Subscription to term deposit (binary)

> Dataset is not committed to the repository. See the notebook for the download/source reference.

## Approach
1. Data sanity checks and target inspection  
2. Preprocessing: scaling and encoding  
3. Model training and validation  
4. Evaluation with class-imbalance aware metrics  
5. Interpretation and business insights  

## Results
See the notebook for detailed metrics and visualizations.

## Limitations & Next Steps
- Cost-sensitive optimization
- Temporal validation
- Batch or API deployment for campaign scoring

## How to Run
```bash
git clone https://github.com/RackLabz/bank-marketing-business-analytics.git
cd bank-marketing-business-analytics

pip install -r requirements.txt
jupyter notebook
```

## Author
Ugwuoke Shedrack Chinonso  
GitHub: https://github.com/RackLabz  
LinkedIn: https://www.linkedin.com/in/shedrack-chinonso-69058219a
