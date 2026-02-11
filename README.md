# 🌾 Crop Production Prediction in India

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/ML-Regression-orange)](https://github.com/ahmedbilal9)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle)](https://www.kaggle.com/datasets/abhinand05/crop-production-in-india/data)

## 📌 Project Overview

A comprehensive **agricultural data science project** that analyzes and predicts crop production across India using machine learning regression techniques. This project leverages historical agricultural data to build predictive models that help understand how **state, district, crop type, season, and cultivated area** influence crop yields.

**Achievement**: Attained **R² = 0.998** with Random Forest, demonstrating exceptional predictive accuracy for agricultural planning and policy-making.

---

## 🎯 Objectives

- Analyze historical crop production trends across Indian states and districts
- Identify key factors influencing crop yields
- Build high-accuracy regression models for production forecasting
- Compare multiple ML algorithms to determine optimal approach
- Provide insights for agricultural policy and resource allocation

---

## 📂 Dataset

**Source**: [Crop Production in India – Kaggle](https://www.kaggle.com/datasets/abhinand05/crop-production-in-india/data)

### Features

| Column | Description | Type |
|--------|-------------|------|
| **State_Name** | Indian state/territory | Categorical |
| **District_Name** | District within state | Categorical |
| **Crop_Year** | Year of cultivation (1997-2015) | Numerical |
| **Season** | Cropping season (Kharif, Rabi, etc.) | Categorical |
| **Crop** | Crop type (Rice, Wheat, Cotton, etc.) | Categorical |
| **Area** | Cultivated area (hectares) | Numerical |
| **Production** | Crop production (metric tons) | Numerical (Target) |

**Dataset Statistics:**
- **Rows**: 246,091 records
- **States**: 33+
- **Crops**: 100+ varieties
- **Time Period**: 1997-2015

---

## 🔬 Methodology

### 1. Data Preprocessing
- **Missing Value Handling**: Removed incomplete records
- **Duplicate Removal**: Ensured data integrity
- **Feature Encoding**: One-hot encoding for categorical variables
- **Feature Scaling**: StandardScaler for numerical features
- **Train-Test Split**: 80% training, 20% testing

### 2. Exploratory Data Analysis (EDA)
- **State-wise Production**: Identified top producing states
- **District-level Analysis**: Regional production patterns
- **Crop-specific Trends**: Yield variations by crop type
- **Seasonal Patterns**: Kharif vs. Rabi season comparison
- **Temporal Analysis**: Production trends over years
- **Correlation Analysis**: Area vs. Production relationships

### 3. Machine Learning Models

Four regression algorithms were implemented:

#### **1. Random Forest Regressor** ⭐ Best Model
- **R² Score**: **0.998**
- **Performance**: Explains ~99.8% of variance
- **Strengths**: Robust to overfitting, handles non-linearity
- **Hyperparameters**: n_estimators=100, max_depth=None

#### **2. XGBoost Regressor**
- **R² Score**: High (close to Random Forest)
- **Performance**: Competitive predictive power
- **Strengths**: Fast training, feature importance
- **Hyperparameters**: n_estimators=100, learning_rate=0.1

#### **3. Decision Tree Regressor**
- **R² Score**: Moderate
- **Performance**: Better than linear but overfitting risk
- **Strengths**: Interpretable, fast inference

#### **4. Linear Regression**
- **R² Score**: Lower
- **Performance**: Baseline model
- **Limitations**: Cannot capture non-linear relationships

### 4. Model Evaluation

**Metrics Used:**
- **R² Score**: Coefficient of determination
- **RMSE**: Root Mean Squared Error
- **MAE**: Mean Absolute Error
- **Cross-Validation**: 5-fold CV for robustness

---

## 📊 Results & Model Comparison

| Model | R² Score | RMSE | Performance | Best For |
|-------|----------|------|-------------|----------|
| **Random Forest** | **0.998** ✅ | Lowest | Exceptional | Production predictions |
| XGBoost | ~0.995 | Very Low | Excellent | Fast inference |
| Decision Tree | ~0.85 | Moderate | Good | Interpretability |
| Linear Regression | ~0.60 | High | Baseline | Simple relationships |

**Key Findings:**
- ✅ **Random Forest** is the most reliable model with **99.8% accuracy**
- ✅ Ensemble methods (RF, XGBoost) vastly outperform linear models
- ✅ Non-linear relationships dominate agricultural production patterns
- ✅ Area is the strongest predictor of production

---

## 📈 Visualizations

The project includes comprehensive visualizations:

1. **Geographic Analysis**
   - State-wise production heatmaps
   - District-level top producers
   - Regional comparison charts

2. **Temporal Patterns**
   - Year-over-year production trends
   - Seasonal production cycles
   - Growth rate analysis

3. **Crop Analysis**
   - Crop-wise production distribution
   - Top 10 crops by yield
   - Crop diversity by region

4. **Correlation Studies**
   - Area vs. Production scatter plots
   - Feature correlation heatmaps
   - Multivariate relationships

5. **Model Performance**
   - Predicted vs. Actual plots
   - Residual analysis
   - Feature importance charts

👉 **Detailed visuals are available in the Jupyter notebook.**

---

## 🛠️ Technologies & Tools

**Programming & Libraries:**
- **Python 3.8+**
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (Random Forest, Decision Tree, Linear Regression)
- **Gradient Boosting**: XGBoost
- **Statistical Analysis**: SciPy

**Development Environment:**
- Jupyter Notebook
- Google Colab (optional)

---

## 🚀 Installation & Usage

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
```

### Running the Project

#### Option 1: Local Execution
```bash
# Clone the repository
git clone https://github.com/ahmedbilal9/Crop-Production-Prediction-in-India-using-Machine-Learning.git
cd Crop-Production-Prediction-in-India-using-Machine-Learning

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook crop-production-prediction-in-india.ipynb
```

#### Option 2: Google Colab
1. Upload notebook to Google Colab
2. Upload dataset or connect to Kaggle API
3. Run cells sequentially

### Project Structure
```
├── data/
│   └── crop_production.csv
├── notebooks/
│   └── crop-production-prediction-in-india.ipynb
├── src/
│   ├── preprocessing.py
│   ├── eda.py
│   ├── modeling.py
│   └── evaluation.py
├── results/
│   ├── figures/
│   └── metrics.json
├── requirements.txt
└── README.md
```

---

## 🌱 Key Insights

### Agricultural Patterns:
1. **Top Producing States**: Uttar Pradesh, Maharashtra, Punjab
2. **High-Yield Crops**: Sugarcane, Rice, Wheat
3. **Seasonal Trends**: Kharif season dominant for rice; Rabi for wheat
4. **Area-Production Correlation**: Strong linear relationship (r > 0.95)

### Model Insights:
- **Feature Importance**: Area > State > Crop Type > Season > Year
- **Non-linearity**: Tree-based models capture complex interactions
- **Generalization**: High cross-validation scores indicate robustness

---

## 🔮 Future Enhancements

- [ ] **Climate Integration**: Incorporate rainfall, temperature, CO₂ data
- [ ] **Time-Series Forecasting**: LSTM, Prophet for temporal predictions
- [ ] **Geospatial Analysis**: GIS mapping of production patterns
- [ ] **Real-Time Dashboard**: Streamlit/Dash for interactive exploration
- [ ] **Deep Learning**: Neural networks for complex feature interactions
- [ ] **Policy Simulation**: What-if analysis for agricultural interventions
- [ ] **Mobile App**: Farmer-facing prediction tool

---

## 📚 References

1. Kaggle Dataset: [Crop Production in India](https://www.kaggle.com/datasets/abhinand05/crop-production-in-india/data)
2. Ministry of Agriculture, Government of India
3. Scikit-learn Documentation: https://scikit-learn.org
4. XGBoost Documentation: https://xgboost.readthedocs.io
5. Agricultural Economics Literature

---

## 🤝 Contributing

Contributions are welcome! Areas for collaboration:
- Additional feature engineering
- Advanced ML models (Neural Networks, Ensembles)
- Visualization enhancements
- Domain-specific validation

**How to Contribute:**
1. Fork the repository
2. Create feature branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add enhancement'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👤 Author

**Ahmed Bilal**  
Electrical Engineering Student | AI/ML Researcher | Agricultural Analytics Enthusiast

- 🌐 [GitHub](https://github.com/ahmedbilal9)
- 💼 [LinkedIn](https://linkedin.com/in/ahmedbilal9)
- ✉️ ahmedbilalned@gmail.com
- 📝 [Medium](https://medium.com/@ab459047)

---

## 🙏 Acknowledgments

- Kaggle community for dataset provision
- Indian Ministry of Agriculture for data collection
- Open-source ML community
- Agricultural domain experts

---

## 📊 Performance Summary

```
✨ Model Accuracy: 99.8% (R² = 0.998)
📈 Predictions: Highly reliable for agricultural planning
🌾 Impact: Supports data-driven farming decisions
🎯 Use Case: Policy-making, resource allocation, yield forecasting
```

---

*"Transforming agricultural data into actionable insights through machine learning for sustainable food security."*