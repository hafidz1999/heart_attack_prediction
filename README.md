Source: https://www.kaggle.com/datasets/ankushpanday2/heart-attack-prediction-in-indonesia/data

# Heart Attack Risk Prediction - Indonesia

A machine learning project aimed at helping doctors quickly assess heart attack risk using accessible patient data—cutting down the need for lengthy and expensive tests. This tool can be deployed onsite, especially in areas with limited medical resources.

## Objective

**Problem**  
Current heart attack screening methods are expensive and time-consuming.

**Goal**  
Build an AI model that helps medical professionals make faster decisions on-site using a quick questionnaire or digital form.

---

## Dataset

**Source**: [Heart Attack Prediction in Indonesia – Kaggle](https://www.kaggle.com/datasets/ankushpanday2/heart-attack-prediction-in-indonesia/data)  
**Shape**: 158,355 rows × 28 columns  
**Notes**:
- Missing values in some features (e.g., `alcohol_consumption`)
- Feature distribution visualized and cleaned
- Strong feature selection via statistical tests:
  - Chi-Squared for categorical variables
  - Mann-Whitney U for numerical variables

---

## Methodology

### Data Preprocessing
- Feature engineering (e.g., grouped age ranges, sleep hours)
- Encoding categorical variables
- Imputation for missing values
- Addressed class imbalance with **SMOTE**

### Model
- **Random Forest Classifier**
- Feature selection based on statistical significance
- Hyperparameter tuning via RandomizedSearchCV

### Evaluation Metrics
- Accuracy: `0.70`
- Precision: `0.60`
- Recall (Sensitivity): `0.76`
- Learning Curve analysis
- Feature importance visualization
- Threshold tuning

---

## Success Criteria

| Metric      | Target | Achieved |
|-------------|--------|----------|
| Accuracy    | ≥ 0.70 | ✅ 0.70   |
| Precision   | ≥ 0.70 | ⚠️ 0.60   |
| Recall (FN) | ≥ 0.75 | ✅ 0.76   |

---

## Technologies

- Python
- Scikit-learn
- Pandas, NumPy
- Seaborn, Matplotlib
- Imbalanced-learn (SMOTE)
- Jupyter Notebook / Google Colab

---

## Impact & Use Case

- Reduces cost by minimizing the need for on-site medical specialists.
- Potential for **mass deployability**, similar to COVID testing models.
- Can support **mobile health units** in underserved or rural areas.

---

## Limitations & Risk

- Should **only be used alongside a medical professional's diagnosis**.
- Risk of **false positives/negatives** if used in isolation.
- The model reflects the **biases and limitations of the dataset**.

---

## Future Work (if possible)

- Deploy as a mobile app (via Streamlit or Flask)
- Add explainability (SHAP/ELI5) to help doctors trust the predictions
- Integrate with national health data for real-time risk mapping

---

## Acknowledgements

Developed by **Hafidz Abdurrafi**  
Special thanks to open data providers and machine learning communities.

---

## License

MIT License
