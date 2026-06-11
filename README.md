# daily-commit-workflow
---
Target Encoding / Label Encoding
If you have categorical columns (for example class = STAR/GALAXY/QSO):
For CatBoost:
Python
cat_features = [...]
No encoding needed.
For XGBoost:
Use LabelEncoder or OneHotEncoding depending on the feature.
Based
