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
Based only on this correlation matrix
My priority order would be:
Keep all original features
Add color-index features (u_g, g_r, r_i, i_z)
Train XGBoost baseline
Check feature importance
Remove only genuinely useless features
Hyperparameter tuning
For Kaggle competitions, feature engineering usually gives a bigger gain than removing correlated features when using XGBoost/CatBoost. The color-index features are the first thing I'd test.
