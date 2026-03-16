# 📈 Retail Demand Forecasting: Predictive AI Model

## 🎯 The Business Problem
For retail stores and local food businesses, accurately predicting daily unit sales is the difference between profitability and massive inventory waste. Over-ordering leads to spoilage and lost capital, while under-ordering leads to sold-out items and lost revenue. 

This project builds a predictive machine learning pipeline using historical transaction data to forecast daily demand for specific items across multiple store locations, allowing businesses to optimize their procurement and supply chain.

## 🛠️ Tools & Technologies
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Random Forest Regressor, GridSearchCV)
* **Data Visualization:** Matplotlib

## 🧠 Methodology
1. **Data Preprocessing:** Extracted temporal features (Day, Month, Year) from raw date strings to capture seasonal buying trends.
2. **Feature Engineering:** Implemented One-Hot Encoding (`pd.get_dummies`) for Store IDs and SKU IDs to prevent the model from assuming false mathematical relationships between categorical identifiers.
3. **Outlier Handling:** Identified and removed extreme sales anomalies (e.g., one-off spikes of 2,800+ units) using percentile thresholds to prevent the model from skewing its baseline predictions.
4. **Model Training:** Utilized a `RandomForestRegressor` to capture non-linear relationships between base prices, promotions, and sales volume.

## 📊 Model Evaluation & Hyperparameter Tuning
The model was evaluated using **Root Mean Squared Error (RMSE)** instead of standard accuracy or R-squared. RMSE was specifically chosen because it mathematically penalizes massive prediction errors, which translates directly to avoiding catastrophic over-ordering or under-ordering in a real-world supply chain.

After establishing a baseline model, I utilized `GridSearchCV` to systematically fine-tune the algorithm's hyperparameters.

**Final Tuned Parameters:**
* `n_estimators`: 20
* `min_samples_split`: 2
* **Performance:** Achieved an $R^2$ score of ~0.82 with a significantly minimized RMSE, proving the model can reliably explain over 80% of the variance in retail demand.

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). 

## 🌟 About Me

Hi there! I'm **Shubham Parikh**. I am a Computer Engineer who understands both technology and business operations. Instead of focusing only on code, I focus on how systems, data, and processes work together to improve business performance.

![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shubhamparikh/)
