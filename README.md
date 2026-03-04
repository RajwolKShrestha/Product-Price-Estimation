# Product Pricing Analysis - Machine Learning Project

**Author:** Rajwol Kumar Shrestha (Roll: KCE081BCT032)  
**Course:** Data Science Project  
**Submitted to:** Sushil Dyopala

## Project Overview

This project develops a predictive model for product pricing in the consumer electronics market, specifically focusing on laptops and PC components. The analysis includes comprehensive exploratory data analysis (EDA), feature engineering, and preprocessing pipeline to prepare data for machine learning models.

## Problem Statement

In the competitive consumer electronics market, determining optimal product pricing is a complex challenge that involves balancing multiple factors including:
- Production costs and hardware specifications  
- Market demand and competitor strategies
- Brand positioning and seasonal trends

This project addresses the need for a data-driven pricing model that can accurately predict product prices and identify key pricing factors.

## Dataset

- **Source:** `product_pricing_market.csv`
- **Size:** 10,000+ product records
- **Features:** Hardware specifications, costs, market dynamics, temporal factors
- **Target:** Final Price ($)

## Project Structure

```
├── DS_Project_KCE081BCT032.ipynb    # Main analysis notebook
├── product_pricing_market.csv        # Original dataset
├── final_dataset_standard_scaled.csv # Processed dataset for ML
├── requirements.txt                   # Python dependencies
├── TASK_8_FEATURE_ENGINEERING_EXPLANATION.md # Feature engineering guide
└── README.md                         # This file
```

## Key Analyses Completed

### 1. Exploratory Data Analysis (EDA)
- ✅ Dataset overview and statistical summaries
- ✅ Missing value analysis and treatment
- ✅ Duplicate detection and removal
- ✅ Distribution analysis for numeric and categorical features
- ✅ Correlation analysis and multicollinearity detection

### 2. Data Visualization
- ✅ Price distribution by categories and brands
- ✅ Feature correlation heatmaps
- ✅ Temporal pricing trends
- ✅ Market dynamics visualization

### 3. Feature Engineering & Preprocessing
- ✅ Domain-informed feature selection
- ✅ Data leakage detection and removal
- ✅ Feature reduction using correlation analysis
- ✅ Dimensionality reduction with PCA

### 4. Data Preprocessing Pipeline
- ✅ Normality testing (before scaling)
- ✅ Feature scaling (StandardScaler & MinMaxScaler)
- ✅ Post-scaling validation and verification
- ✅ Feature distribution visualization

## Key Findings

### Data Quality
- **No missing values** after preprocessing
- **No duplicate records** found
- **20 features** selected after feature reduction
- **10,000 samples** ready for training

### Feature Insights
- **Screen Size** (r=0.609) - Strongest hardware predictor
- **Battery Capacity** (r=0.578) - Second strongest predictor  
- **Weight** (r=0.557) - Important for pricing decisions
- **Data Leakage Features Removed:** Profit_Margin_%, Price_to_Demand_Ratio

### Scaling Results
- ✅ **StandardScaler:** All features normalized (Mean≈0, Std≈1)
- ✅ **Distributions improved** after scaling
- ✅ **Ready for linear models** (Ridge, Lasso, Linear Regression)

## Files Generated

### Processed Datasets
- `final_dataset_standard_scaled.csv` - StandardScaled features + target
- Ready for immediate model training

### Analysis Outputs
- Comprehensive EDA visualizations
- Feature correlation matrices  
- Distribution plots after scaling
- Statistical summaries and insights

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib/Seaborn** - Data visualization
- **Scikit-learn** - Preprocessing and PCA
- **Scipy** - Statistical analysis
- **Jupyter Notebook** - Interactive development

## Next Steps

### Recommended Model Training Pipeline
1. **Train-Test Split** (80/20, stratified by price quartiles)
2. **Model Training:** 
   - Linear Regression (baseline)
   - Ridge/Lasso Regression (regularized)
   - Random Forest (ensemble)
   - Gradient Boosting (advanced ensemble)
3. **Hyperparameter Tuning** with Cross-Validation
4. **Model Evaluation** and selection
5. **Final validation** on test set

### Expected Performance
- **Baseline R²:** ~0.70 (current feature set)
- **Target R²:** 0.85+ (with hyperparameter tuning)
- **Error Reduction:** 30-40% improvement expected

## Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Data Science
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis:**
   ```bash
   jupyter notebook DS_Project_KCE081BCT032.ipynb
   ```

4. **Use processed data:**
   ```python
   import pandas as pd
   df = pd.read_csv('final_dataset_standard_scaled.csv')
   ```

## Contributing

This is an academic project for coursework submission. For questions or suggestions, please contact the author.

## License

This project is created for educational purposes as part of academic coursework.

---

**Last Updated:** March 4, 2026  
**Status:** Data Preprocessing Complete ✅ | Ready for Model Training 🚀