# Crop Production Prediction in India

## 📌 Project Overview
This project explores and predicts **crop production in India** using historical agricultural data. The primary objective is to analyze how various factors such as **state, district, crop, season, area, and year** affect production, and to build robust machine learning models that can provide reliable predictions.

---

## 📂 Dataset
- **Source**: [Crop Production in India – Kaggle](https://www.kaggle.com/datasets/abhinand05/crop-production-in-india/data)
- **Features**:
  - `State_Name`, `District_Name` — geographic identifiers
  - `Crop_Year` — year of cultivation
  - `Season` — cropping season
  - `Crop` — crop type
  - `Area` — cultivated area (in hectares)
  - `Production` — crop production (in metric tons)

---

## 🔎 Methodology
1. **Data Preprocessing**
   - Cleaned missing values
   - Dropped irrelevant attributes
   - Applied one-hot encoding to categorical variables

2. **Exploratory Data Analysis (EDA)**
   - State-wise and district-wise production trends
   - Crop-specific and season-wise comparisons
   - Correlation between cultivated area and production

3. **Machine Learning Models**
   Four regression models were implemented and compared:
   - **Random Forest Regressor**
   - **Linear Regression**
   - **Decision Tree Regressor**
   - **XGBoost Regressor**

   - **Evaluation Metrics**: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² Score
   - **Train-Test Split**: 80% / 20%

---

## 📊 Results & Comparison
The performance of the four models is summarized below:

| Model                 | R² Score | Notes |
|-----------------------|----------|-------|
| **Random Forest**     | **0.998** | Best performing model, explains ~99.8% of variance in crop production |
| Linear Regression     | Lower     | Struggled with nonlinear relationships; underperformed significantly compared to ensemble methods |
| Decision Tree         | Moderate  | Performed better than Linear Regression but showed overfitting tendencies |
| XGBoost               | High      | Competitive with Random Forest, but slightly lower predictive power in this dataset |

✅ **Conclusion**: Random Forest Regressor is the most reliable model for this dataset, offering excellent prediction accuracy.

---

## 📈 Visualizations
The notebook provides a variety of plots and visual insights:
- State-wise production
- District-level top producers
- Seasonal comparisons
- Crop year trends
- Area vs. Production regression

👉 **Detailed visuals are available in the notebook.**

---

## 🚀 Future Work
- Incorporate climatic variables (rainfall, temperature, CO₂) for improved accuracy
- Explore time-series forecasting approaches (e.g., LSTM, Prophet)
- Build an interactive dashboard for stakeholders and policymakers

---

## 🛠️ Skills & Tools
- **Programming**: Python (Pandas, NumPy)
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (Random Forest, Linear Regression, Decision Tree), XGBoost
- **Other**: Data Cleaning, EDA

---

## ▶️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/crop-production-prediction.git
   cd crop-production-prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook crop-production-prediction-in-india.ipynb
   ```

---

## 📜 License
This project is licensed under the MIT License.

